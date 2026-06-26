# Nexus Events — Admin Dashboard

A Firebase-powered web platform for managing events, teams, and attendees — built for organizers who need speed and clarity.

## Features

- **Event Management** — Create, track and archive events with location pinning via Mapbox
- **Live Check-in Tracking** — Monitor attendee counts and check-ins in real time
- **Team Management** — Add and manage team members under your organization
- **Data Export** — Export event/attendee data to Excel with one click
- **Secure Auth** — Firebase Authentication with role-based access control

## Tech Stack

- **Frontend**: Vanilla JS, HTML5, CSS3
- **Backend**: Firebase (Firestore, Auth, Hosting, Cloud Functions)
- **Maps**: Mapbox GL JS
- **Grid**: AG Grid Community
- **Export**: SheetJS (xlsx)

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v14+
- [Firebase CLI](https://firebase.google.com/docs/cli)

### Setup

```bash
# 1. Clone this repo
git clone https://github.com/YOUR_USERNAME/nexus-events.git
cd nexus-events

# 2. Install Firebase CLI (if not already)
npm install -g firebase-tools

# 3. Login to Firebase
firebase login

# 4. Create a new Firebase project at https://console.firebase.google.com
#    Then update .firebaserc with your project ID

# 5. Install Cloud Functions dependencies
cd functions
npm install
cd ..

# 6. Deploy to Firebase Hosting
firebase deploy
```

### Local Development

```bash
firebase emulators:start
```
Then open `http://localhost:5000` in your browser.

## Project Structure

```
nexus-events/
├── public/
│   ├── index.html          # Main dashboard shell
│   ├── login.html          # Login page
│   ├── signup.html         # Registration page
│   ├── create.html         # Create event form (partial)
│   ├── ongoing.html        # Active events table (partial)
│   ├── past.html           # Past events table (partial)
│   ├── css/main.css        # All styles
│   └── js/
│       ├── app.js          # Core logic & Firebase calls
│       └── index.js        # Dashboard routing
├── functions/
│   └── index.js            # Cloud Functions
├── firestore.rules         # Firestore security rules
└── firebase.json
```

## Screenshots

<!-- Add your own screenshots here after deploying -->

## License

MIT
