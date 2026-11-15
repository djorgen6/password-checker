# 🔐 Password Strength Checker

An interactive password security tool built to explore password strength, entropy, and theoretical password-cracking times.

**Live Demo:** https://djorgen6.github.io/password-checker/

## About the Project

I created this project to apply programming to practical cybersecurity concepts and better understand what makes passwords difficult to crack.

The tool allows users to adjust password length, select different character types, and compare estimated cracking times against different attacker models. The goal was to make concepts like password entropy and brute-force attacks easier to understand through an interactive demonstration.

## Features

- **Password Length:** Adjustable from 4 to 32 characters.
- **Character Selection:** Enable or disable lowercase letters, uppercase letters, numbers, and symbols.
- **Attacker Models:** Compare estimated cracking times using a Basic CPU, GPU Attack, or Advanced Cluster.
- **Entropy Calculation:** Estimates password entropy in bits based on length and available character combinations.
- **Strength Indicator:** Displays a visual strength bar based on the estimated cracking time.
- **Shareable Configurations:** Generates URLs that preserve the selected settings, allowing others to view the same configuration.

## Technologies Used

- **HTML5** – Page structure, content, and interactive controls.
- **CSS3** – Styling, layout, and visual components.
- **JavaScript** – Password calculations, event handling, and interactive functionality.
- **URLSearchParams API** – Saves and restores configurations through URL parameters.
- **GitHub Pages** – Hosting and deployment.

The project is contained in a single `index.html` file, with HTML, CSS, and JavaScript together. It does not require a separate backend or framework. An external zxcvbn library is included through a CDN, although the current calculations use a separate custom implementation.

## How It Works

The checker uses a simplified mathematical model to estimate password complexity and theoretical cracking times.

1. **Character Pool:** Determines the number of possible characters based on the selected character types.
2. **Entropy:** Estimates password entropy using:

   `Entropy = Password Length × log₂(Character Pool)`

3. **Attacker Model:** Assigns an assumed guessing speed to the selected attacker:
   - Basic CPU: 10⁷ guesses/second
   - GPU Attack: 10¹⁰ guesses/second
   - Advanced Cluster: 10¹² guesses/second
4. **Cracking Time:** Divides the total possible combinations by the assumed guessing speed.
5. **Visual Feedback:** Converts the estimated time into a simplified strength score displayed through a progress bar.

## Development & AI Assistance

I developed this project with assistance from **ChatGPT (OpenAI)** around the time of its original development and GitHub publication.

I used ChatGPT as a development aid for JavaScript implementation, mathematical calculations, troubleshooting, and refining functionality. Development was an iterative process of working through ideas, testing implementations, and improving the tool.

## Limitations & Accuracy

This project is primarily a learning and demonstration tool, not a professional password auditing application. Its calculations are simplified theoretical estimates and may not accurately represent real-world password security or attack conditions.

It does not account for every attack method, including dictionary attacks, leaked credentials, password reuse, or predictable patterns. Actual password security depends on more than character variety alone.

Results should be treated as educational estimates, not guarantees of security.

**Never enter passwords that you actually use.**

## Purpose & Takeaways

This project gave me an opportunity to explore password security through hands-on development while applying concepts such as entropy, brute-force attacks, and computational complexity.

It also demonstrates how fundamental web technologies can be used to build an interactive cybersecurity application and how AI tools can assist with learning, development, and problem-solving.

---

**Developed by Daniel Jorgensen**

[@djorgen6](https://github.com/djorgen6)
