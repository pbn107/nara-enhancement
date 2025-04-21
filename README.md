# CIS 3500: Nara Extension Starter

## Overview
This assignment involves enhancing a Chrome extension developed by one of the Top 3 winners of the MCIT hackathon. The project provides hands-on experience in web development, API integration, and collaborative coding.

**Original project:** [Nara](https://github.com/luyiZhang818/Nara-Chrome-Extension)

## Project Description
Nara is a Chrome extension that helps users manage their tasks and reminders efficiently. Your task is to enhance this extension by implementing new features.

## Enhancement Options
Choose one of the following enhancements to implement:

1. **Speech Bubble Encouragement**: Implement a feature where, whenever the user checks off a task, a speech or thought bubble appears near the deer with a short, encouraging message (e.g., “Great job!”, “You’re making progress!”, “Keep going!”).
2. **Daily Gratitude Log**: Implement a small text area where users can note one thing they’re grateful for each day. Over time, they can revisit a dedicated “gratitude log” to see their positive moments. Provide an interesting method to save these entries and display them on a separate screen so users can easily access their past entries.
3. **Mood Selection Prompt**: Implement a simple mood selection feature(e.g., happy, stressed, neutral) with a small icon or emoji. This allows users to log their emotional state quickly each day.
4. **Rotating Weekly Challenge**: Implement a weekly challenge system—such as “Drink 8 glasses of water each day” or “Take a 10-minute walk daily.” Users can check off these mini-challenges alongside their normal tasks for extra motivation.
5. **Inspirational Quote Overlay**: Implement a short inspirational quote or positive affirmation that appears on each new tab, displayed in a subtle text overlay.
6. **Implement a History Feature**: Maintain a log of all tasks and reminders created by the user, allowing them to revisit past items and track progress over time.
7. **Custom Feature**: Propose a unique feature (requires instructor/TA approval).

## Getting Started

### Step 1: Team Organization
- Assign a team member as the **Product Manager (PM)** for Nara.
- Ensure this PM is different from the one assigned to the Lunch Lotto project.

### Step 2: Repository Setup
The PM should fork the repository:
1. Navigate to the `nara-extension-starter` repository on GitHub.
2. Click the **Fork** button to create a copy under their account.

### Step 3: Cloning the Repository
Once the PM has forked the repository, team members should clone it locally:
```sh
git clone https://github.com/<PM-username>/nara-extension-starter.git
```

### Step 4: Development Workflow
1. Open the project in a text editor (e.g., **Visual Studio Code** recommended).
2. Make changes to the codebase.
3. Use the following commands to commit and push your changes:

```sh
git add .
git commit -m "feat: [feature name] added"
git push
```

4. As team members contribute, collaborate using **Pull Requests (PRs)** on GitHub.
5. Regularly sync your local repository with the latest changes:

```sh
git pull
```

6. Resolve merge conflicts as needed and ensure smooth integration.

## Submission
- Submit the final version of your project as per course guidelines.
- Include a brief write-up of your implemented features and any challenges faced.

---
Happy coding, and good luck with Nara! 🦌

## 1. Speech‑Bubble Encouragement  
Whenever the user completes a task, a brief, positive message “pops up” above the checked item to reinforce good habits and boost motivation.  
- **Randomized Messages**  
  A small set of encouraging phrases (e.g. “Great job!”, “You’re making progress!”, “Keep going!”) is chosen at random each time.  
- **Contextual Positioning**  
  The bubble is positioned just above the task in the list, making it clear which action triggered the praise.  
- **Animated Fade‑Out**  
  Each bubble uses a CSS transition to appear instantly, then fade out smoothly over 0.8 seconds before being removed from the DOM.  

### 2. Daily Gratitude Log  
A dedicated modal allows users to record one thing they’re grateful for each day, fostering mindfulness and positive reflection.  
- **Seamless Entry**  
  Click **“Add Gratitude”** to open a modal with a labeled textarea. Users type their entry and click **Save**, which stores the text under today’s date in `chrome.storage.local`.  
- **Persistent Storage**  
  Entries are saved by ISO date (e.g. `2025-04-20`) and remain available even after the browser is closed or the extension is reloaded.  
- **History View**  
  The **“View Gratitude Log”** button opens a scrollable modal listing all past entries, newest first. Each entry displays the date in bold followed by the user’s text.  
- **Responsive Styling**  
  Both entry and history modals are styled for clarity: a semi‑transparent dark overlay, a centered white content box with rounded corners, clear labels, and accessible focus states.  

---

