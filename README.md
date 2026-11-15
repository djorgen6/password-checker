# 🔐 Password Strength Checker

A browser-based cybersecurity project exploring password strength, entropy, and theoretical password-cracking times.

**Live Demo:** https://djorgen6.github.io/password-checker/

## About the Project

I built this project to explore password security and demonstrate how password length, character variety, and attacker computing power influence password strength.

The tool allows users to configure a theoretical password and see how its complexity affects entropy and estimated cracking time under different attacker models.

The goal was to turn cybersecurity concepts into something interactive and easy to understand.

## Features

- **Password Length:** Adjustable from 4 to 32 characters.
- **Character Selection:** Enable or disable lowercase letters, uppercase letters, numbers, and symbols.
- **Attacker Models:** Compare estimated cracking times against a basic CPU, GPU attack, or advanced computing cluster.
- **Entropy Calculation:** Estimates password entropy in bits using the available character pool and password length.
- **Strength Indicator:** Displays a visual strength bar based on the calculated cracking-time estimate.
- **Shareable Configurations:** Generates shareable URLs that preserve the selected settings.

## Technologies Used

- **HTML5** – Page structure and user interface.
- **CSS3** – Styling, layout, and visual components.
- **JavaScript** – Password calculations, interactive controls, and URL parameter handling.
- **URLSearchParams API** – Saves and restores configurations through URL parameters.
- **GitHub Pages** – Hosting and deployment.

The project uses a single `index.html` file containing the HTML, CSS, and JavaScript, without a separate backend or framework.

## How It Works

The checker uses a simplified mathematical model to estimate password security.

1. **Character Pool:** Calculates the possible character combinations based on the selected character types.
2. **Entropy:** Estimates theoretical entropy using:

   `Entropy = Password Length × log₂(Character Pool)`

3. **Attacker Model:** Assigns a theoretical guessing speed based on the selected attacker:
   - Basic CPU: 10⁷ guesses/second
   - GPU Attack: 10¹⁰ guesses/second
   - Advanced Cluster: 10¹² guesses/second
4. **Cracking Time:** Divides the total possible combinations by the assumed guessing speed.
5. **Visual Feedback:** Converts the estimated time into a simplified strength score displayed through a progress bar.

## Development & AI Assistance

This project was developed with assistance from **ChatGPT (OpenAI)** around the time of its original development and GitHub publication.

ChatGPT was used as a development aid for working through JavaScript logic, mathematical calculations, implementation ideas, and troubleshooting. The project was built iteratively, with the code and functionality refined throughout development.

AI assistance was used as a tool to support the development process, rather than as a replacement for understanding the underlying concepts.

## Security Considerations

**Accuracy Disclaimer:** This project is intended primarily as a learning and demonstration tool, not a definitive password security evaluator. Its entropy calculations and estimated cracking times are simplified theoretical models and may not accurately represent real-world password security or attack conditions. Results should be treated as educational estimates rather than guarantees.

This project is an educational demonstration, not a production-grade password auditing tool.

Cracking times are theoretical estimates based on assumed guessing speeds and do not account for every real-world attack technique, such as dictionary attacks, leaked credentials, password reuse, or advanced pattern recognition.

Actual password security depends on more than character variety alone. Longer, unique passwords and passphrases are generally preferable.

**Never enter passwords that you actually use.**

## Purpose & Takeaways

This project provided an opportunity to apply programming to practical cybersecurity concepts, particularly password entropy, brute-force attacks, computational limitations, and security awareness.

It also demonstrates how basic web technologies can be used to build an interactive security-focused application and how AI tools like ChatGPT can assist with learning, development, and problem-solving.

---

**Developed by Daniel Jorgensen**  
GitHub: [@djorgen6](https://github.com/djorgen6)
