# Matter Master — Live Teacher-Paced Edition

This version uses Firebase Realtime Database so the teacher and students can share live room state.

## What it does
- Teacher creates a random 4-character room code.
- Teacher page automatically generates a student join link.
- Students enter a nickname + room code.
- Teacher controls Start Question, Next Question, Show Results, and Hide Results.
- Students cannot advance the game themselves.
- Student responses include P-A-W distractor analysis.
- XP and streaks are tracked per student.
- Class response data appears on the teacher dashboard.
- Content is S8P1.a–f and stays at Grade 8 level.

## One-time setup

1. Create a Firebase project.
2. Register a Web App.
3. Create Realtime Database.
4. Enable Authentication > Sign-in method > Anonymous.
5. Put your Firebase web app config into `firebase-config.js`.
6. Add the Realtime Database rules from `database.rules.json`.
7. Host the folder on GitHub Pages or another static host.

Firebase's official web setup documentation explains how to register the web app and obtain the configuration object:
https://firebase.google.com/docs/web/setup

Firebase's Realtime Database documentation explains the realtime synchronization used here:
https://firebase.google.com/docs/database/web/start

## Hosting
GitHub Pages can publish a static site from a repository branch. The final site URL follows the GitHub Pages pattern:
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/

Important: GitHub Pages sites are public. Do not put student-identifying information into the site or repository.

## Student link
Once hosted, the student URL is simply:
YOUR-SITE/student.html

The teacher's screen generates the exact room-specific link students should use.

## Security note
The rules require anonymous Firebase authentication. For classroom use, students should use first names, initials, or teacher-approved nicknames—not sensitive information.
