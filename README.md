# dailymotion player workshop (Internal Use Only)

Base material for a workshop to introduce the player API.

This is a step by step guide to introduce dailymotion player integration in a 3rd party web site.

## Setup

Checkout the repository and install required dependencies

``` bash
git clone git@github.com:dailymotion/player-workshop-api.git
# setup dev environement
cd player-workshop-api
npm install
# start a local server and watch the local files for change, and open http://localhost:8002/ in the default browser
npm start
```

Your default browse should open to `http://localhost:8002/`

## Usage

Once the local server is running, you can go through every step of the workshop by checking out different branches (e.g. `git checkout step-5`):
```
(step-0) Step 0 : Naive iframe
(step-1) Step 1 : allowfullscreen
(step-2) Step 2 : QS parameters
(step-3) Step 3 : JavaScript SDK
(step-4) Step 4 : SDK async loading
(step-5) Step 5 : SDK apiready event
(step-6) Step 6 : SDK calling play/pause
(step-7) Step 7 : SDK loading antoher video
(step-8) Step 8 : SDK load without autoplay
```

Alternativelly, you can also copy/paste the content of every file in the `steps` folder to the `index.html`