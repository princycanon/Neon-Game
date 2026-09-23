Create the index.html, style.css, and game.js files for the complete Princy's Neon Race game described below. Generate the code for each file separately. Do not use Agent mode, external frameworks, or external assets. Make everything work locally in a browser.
Build a complete browser game called “Princy’s Neon Race”.

1. GAME CONCEPT

Create a futuristic neon racing/dodging game that runs entirely in a web browser.

The player controls a neon race car on a vertically scrolling highway. Enemy cars and obstacles continuously appear from the top and move downward. The player must dodge them and survive as long as possible.

The game should feel like a polished mini arcade game, not a basic HTML demo.

2. TECHNOLOGY

Use only:

- HTML5
- CSS3
- Vanilla JavaScript

Do NOT use React, Node.js, TypeScript, Bootstrap, external frameworks, or external game engines.

The game must work by opening "index.html" in a browser.

Keep the project organized:

princys-neon-race/
│
├── index.html
├── style.css
├── game.js
├── README.md
└── tests/
    └── neon_race_test.py

3. VISUAL DESIGN

Theme: futuristic neon arcade.

Use a dark background with neon-style UI.

Game screen should contain:

- Game title: PRINCY’S NEON RACE
- Score
- High Score
- Current speed/level
- Start Game button
- Pause button
- Restart button
- Game area
- Game-over screen

Make the interface responsive so it works on desktop and smaller screens.

Use CSS animations for neon effects, glowing text, road movement, and buttons.

Do not rely on external images. Create the car, road, obstacles, and effects using HTML/CSS/Canvas or JavaScript-generated graphics.

4. GAMEPLAY

Create a road in the center of the screen.

The player controls a neon race car.

Desktop controls:

- Left Arrow / A → move left
- Right Arrow / D → move right
- Space → pause/resume

Also provide visible left/right buttons for mobile users.

The player's car must remain inside the road boundaries.

Enemy cars should spawn at random positions on the road and move downward.

The player loses when their car collides with an enemy car.

5. SCORING

Start the score at 0.

Increase the score continuously while the player survives.

Also award bonus points when successfully avoiding enemy cars.

Display:

SCORE: 000000
HIGH SCORE: 000000
LEVEL: 1

Store the high score using browser local storage.

The high score must survive page refreshes.

6. DIFFICULTY

Start relatively easy.

Gradually increase difficulty as the score increases.

Increase:

- Enemy car speed
- Spawn frequency
- Number of obstacles

Introduce levels.

Example:

Level 1 → slow traffic
Level 2 → faster traffic
Level 3 → more traffic
Level 4+ → increasingly difficult

Do not make the game impossible.

7. ROAD EFFECT

Create a vertically moving road.

Use animated lane markings to make the player feel like they are driving forward.

The road should contain 3 lanes.

The player's car should normally occupy one lane, but allow smooth movement between lanes.

Enemy cars should spawn in different lanes.

8. POWER-UPS

Add occasional power-ups.

Include:

Shield

Protects the player from one collision.

Nitro

Temporarily increases movement speed.

Score Boost

Doubles score gained for a short period.

Power-ups should have clear visual indicators.

Display the active power-up status on the screen.

9. GAME STATES

Implement these states:

START
PLAYING
PAUSED
GAME OVER

Start screen:

PRINCY’S NEON RACE

Dodge the traffic.
Survive the neon highway.

[ START RACE ]

Pause screen:

GAME PAUSED

[ RESUME ]
[ RESTART ]

Game-over screen:

RACE OVER

Score: XXXXX
High Score: XXXXX

[ RACE AGAIN ]

10. SOUND

Add optional simple sound effects using browser APIs or generated tones.

Include sounds for:

- Button click
- Collecting power-up
- Collision
- Level increase
- Game over

Provide a:

🔊 SOUND ON/OFF

button.

The game must still work if audio is unavailable or blocked by the browser.

11. PARTICLES AND EFFECTS

Add lightweight visual effects:

- Neon glow
- Speed lines
- Collision particles
- Power-up glow
- Score animation
- Level-up notification

Keep animations efficient so the game runs smoothly on normal college lab computers.

Respect "prefers-reduced-motion".

12. ACCESSIBILITY

Include:

- Keyboard controls
- Visible buttons
- Clear text
- Good contrast
- Accessible button labels
- "aria-live" for score/game status where appropriate

Do not make essential gameplay dependent on hover.

13. MOBILE SUPPORT

The game should work on mobile browsers.

Add large touch controls:

[ ◀ LEFT ]       [ RIGHT ▶ ]

Make buttons easy to tap.

Prevent accidental page scrolling while the game is being played.

14. GAME LOGIC REQUIREMENTS

Use clean JavaScript architecture.

Separate responsibilities into functions/classes where appropriate.

Include functions for:

- Initializing the game
- Starting the game
- Updating the game loop
- Drawing/rendering
- Player movement
- Enemy spawning
- Collision detection
- Score calculation
- Difficulty progression
- Power-ups
- Pause/resume
- Game over
- Restart
- High-score management

Use "requestAnimationFrame()" for the main game loop.

Clean up timers, animation frames, and event listeners when restarting the game.

Avoid global variables where possible.

15. SELENIUM TESTING

Create:

tests/neon_race_test.py

Use Python Selenium.

The Selenium test should verify:

1. The game page loads.
2. The title contains “Princy’s Neon Race”.
3. The Start Game button exists.
4. Clicking Start Game changes the game into the playing state.
5. Score is displayed.
6. Pause button works.
7. Resume works.
8. Restart works.
9. Game-over screen contains a score.
10. The high-score element exists.
11. The mobile control buttons exist.

Use Selenium WebDriver.

Make the test suitable for Chrome/Chromium.

Do not require internet access for the game itself.

16. JENKINS COMPATIBILITY

The project will eventually be tested through Jenkins.

Make sure:

- The project can be cloned from Git.
- Selenium tests can run from the command line.
- Tests return proper exit codes.
- No manual interaction is required for automated tests.
- Avoid dependencies that require an internet connection during the game test.

Create a "README.md" explaining:

Project Overview
Features
Controls
How to Run
How to Run Selenium Tests
Git Commands
Jenkins Integration

17. JENKINS PIPELINE

Also create a basic:

Jenkinsfile

Pipeline stages should be:

Checkout
   ↓
Install Test Dependencies
   ↓
Run Selenium Tests
   ↓
Archive Test Results

Use a simple declarative Jenkins pipeline.

Do not assume Docker is installed.

Do not require Node.js.

Use Python + Selenium for automated testing.

18. CODE QUALITY

Write clean, readable, commented code.

Do not put the entire application into one giant HTML file.

Use:

index.html
style.css
game.js

Keep JavaScript modular and understandable.

Handle errors gracefully.

Do not leave TODO placeholders.

Do not create fake buttons that don't work.

Every visible button must perform its advertised function.

19. FINAL REQUIREMENT

Generate the COMPLETE project files.

After creating them, explain:

1. What each file does.
2. How to run the game locally.
3. How to initialize the Git repository.
4. How to commit and push it to GitHub.
5. How to run the Selenium tests.
6. How to configure Jenkins to automatically clone the GitHub repository and run the tests.

The final result should look and feel like a small professional arcade game named:

🏎️ PRINCY’S NEON RACE

Do not simplify the project into a basic example. Build the complete working version described above.