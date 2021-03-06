# Builder

## About

Builder is backend automation for quickly developing lesson content (currently only supports chess).

Builder is live [here](http://builder.chesstrained.com).

If a valid lesson is submitted, then it will be available on [Square First Chess](http://beta.chesstrained.com/#/simulation).

## Installation Instructions

    cd client

    elm-app install

- Must have [Elm](https://guide.elm-lang.org/install.html) and [create-elm-app](https://github.com/halfzebra/create-elm-app) installed (can also `elm-app eject` if you are more familiar with webpack).
  - Current Elm version is `0.18`.
  - Current create-elm-app version is `v1.10.4` (npm install create-elm-app@v1.10.4)

## Usage

    cd client

    npm run dev

* Need to be running dev-server (or point backend wherever).
* If you have tmux and nodemon then you are also able to use the .tmuxrc automation: `tmux source-file .tmuxrc`

## Directions for actually making a lesson

These are the steps that you need to take to make a lesson:

- Use procedural generation to find original idea (either by clicking regenerate, or by moving slider).
- Rearrange / optimize the board for the start of the lesson (**Must be legal Chess position, i.e. Monarch who's team it is may NOT be in check**).
- Click `Record Lesson`.
- Create a frame
  - Fill in the default text with what you want to be displayed at the beginning of that frame.
  - Optionally; click on squares to create discoverable content (**Currently only supports valid moves for your team**).
  - Make move (Use Chess Api button for opponent).
- Repeat frame creation until satisified with lesson.

Please remember that we are trying to write content that is optimized for the learner.

## Deployment

Use the Terraform script.

## Todo / Next Up

- Integrate with chess api
  - Check for legal position
  - Show possible moves in builder
