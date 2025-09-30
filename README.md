Stego-Riddle Challenge

📌 Project Overview
This project is designed as an interactive web-based puzzle challenge.  
The player is presented with a web page containing 3 images. At first glance, nothing seems unusual.  
However, the real challenge begins when the player inspects the web page’s source code.

---

🕵️ Walkthrough of the Challenge

1. Web Page Inspection  
   - The page displays 3 static images.  
   - On inspecting the page source code, players discover hidden commented sections.

2. Hidden Riddles
   - Inside the commented code, players find riddles.  
   - Solving these riddles gives 6 numbers as answers.

3. Coordinate Pairing
   - The 6 numbers are paired to form 3 coordinate points (x, y).  
   - Example: `(x1, y1), (x2, y2), (x3, y3)`

4. Steganography Hint 
   - These 3 coordinates point to specific pixels in one of the given images.  
   - Each pixel hides part of a 9-digit RGB code using LSB (Least Significant Bit) steganography.

5. Final Reveal 
   - By extracting pixel values from the mentioned coordinates, players reconstruct the hidden RGB code.  
   - This RGB code corresponds to a color.

6. Flag Submission 
   - The flag for this CTF challenge is the color name of the decoded RGB code.  
   - Example: If the code is `#FF0000`, the flag will be RED.

---

🛠️ Tech Stack
- Frontend: HTML, CSS  
- Challenge Logic: Hidden riddles via HTML comments  
- Steganography: LSB (Least Significant Bit) encoding in images  

---

🚀 How to Play
1. Open the web page in your browser.  
2. Inspect the page (Right Click → Inspect or `Ctrl+Shift+I`).  
3. Search for commented sections in the HTML code.  
4. Solve the riddles to get 6 numbers.  
5. Pair the numbers into 3 coordinate points.  
6. Extract the pixel values from the given image using the coordinates.  
7. Combine RGB values → Get the final 9-digit RGB code.  
8. Find the color name of that RGB code → This is the flag.  

---

🎯 Goal
The challenge tests:  
- Observation skills  
- Problem-solving with riddles  
- Understanding of coordinates & pixels  
- Knowledge of image steganography  
- Mapping RGB values → Color names

---

📷 Example:
- Riddle answers: `12, 45, 78, 32, 56, 90`  
- Coordinates: `(12, 45), (78, 32), (56, 90)`  
- Pixel values reveal hidden RGB code → #123456  
- Color name: "DARK SLATE GRAY"
- ✅ Flag: `dark_slate_gray`

---

Good luck, and happy hunting! 🚀

Play the puzzle directly here:  
👉 [https://welcome-to-ctf.netlify.app/]
