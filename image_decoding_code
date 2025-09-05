from PIL import Image
def decode_rgb_code(image_path, coordinates):
    try:
        img = Image.open(image_path)
    except FileNotFoundError:
        print(f"❌ File not found: {image_path}")
        return

    pixels = img.load()
    decoded_digits = ""

    for x, y in coordinates:
        r, g, b = pixels[x, y]
        decoded_digits += f"{r}{g}{b}"

    print("🔓 Decoded RGB code:", decoded_digits)
    return decoded_digits


# Example usage
if __name__ == "__main__":
    choice = input("Do you want to encode or decode? (e/d): ").strip().lower()

    if choice == 'e':
        image_path = input("Enter input image filename (e.g., input.png): ").strip()
        output_path = input("Enter output image filename (e.g., output.png): ").strip()
        rgb_code = input("Enter 9-digit RGB code (only digits): ").strip()
        coordinates = []
        print("Enter 3 coordinates (x y) one per line (e.g., 10 15):")
        for _ in range(3):
            x, y = map(int, input().split())
            coordinates.append((x, y))
        encode_rgb_code(image_path, output_path, rgb_code, coordinates)

    elif choice == 'd':
        image_path = input("Enter image filename to decode from (e.g., output.png): ").strip()
        coordinates = []
        print("Enter 3 coordinates (x y) one per line:")
        for _ in range(3):
            x, y = map(int, input().split())
            coordinates.append((x, y))
        decode_rgb_code(image_path, coordinates)

    else:
        print("❌ Invalid option. Choose 'e' for encode or 'd' for decode.")
