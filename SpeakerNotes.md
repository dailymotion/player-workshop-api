# Speaker Notes

## Preparation

 - You may want to update the videos used as a demo to point to video you own (so you can also demo the user settings)
 - Go to [Settings | Player customization](https://www.dailymotion.com/settings/playercustomization) and remove any custom value
 - Go to [Settings | Logo overlay](https://www.dailymotion.com/settings/logooverlay) and remove any existing logo
 - git checkout the `master` branch and copy/paster content from `steps/0-start.html` in `index.html`
 - remove the `iframe` from `index.html`
 - Run `npm start` to start the local server

## Step 0 : Basic iframe & allowfullscreen

 - Start from a video page. e.g. http://www.dailymotion.com/video/x4r5udv
 - Click on share > embed in the player UI
 - Copy/paste the embed code to `index.html`
 - Explain how the `iframe` attributes are important, especially `allowfullscreen`

## Step 1 : User Settings

 - Go to [Settings | Player customization](https://www.dailymotion.com/settings/playercustomization) and add a few customization (e.g. highlight color, disabled logo)
 - Refresh the page to show how it impacts the player
 - While here, go to [Settings | Logo overlay](https://www.dailymotion.com/settings/logooverlay) and add a custom logo+link
 - Refresh the page again

## Step 2 : player parameters

 - Add some player parameters to customize the `iframe` embed player (`start`, `ui-theme`, `ui-highlight`, `ui-logo`)
 - Explain how _User Settings_ are prioritized against _query string parameters_.
 - Go to [Settings | Player customization](https://www.dailymotion.com/settings/playercustomization) and remove any custom value
 - Refresh the page to show how _query string parameters_ are now applied

## Step 3 : SDK base

 - Remove the `iframe` in favor of the SDK initialization code
 - (or copy from `steps/3-sdk-base.html`)
 - Show how player parameters and video id are still used, but in a different way
 - Explain how the SDK is different from a simple `iframe`, how it provides more control and advanced behaviors
 - Quick word about the SDK _properties_, _events_ and _methods_.

## Step 4 : SDK async (optionnal, depending on the audience)

 - Improve the code to use a non-blocking SDK initialization code
 - Explain how/why it's a better way

## Step 5 : apiready event

 - Call `player.play()` right after player initialization
 - Explain why it doesn't work as expected
 - Move `player.play()` call into an `apiready` event listener
 - Show how it work better but why `autoplay=1` parameter is a better option in that case
 - A word on why programmatic calls on `apiready` event are a bad practice

## Step 6 : play/pause buttons

 - Add disabled play 7 pause buttons
 - Enable then on `apiready` and add an event listener on `click` event
 - Call the corresponding `play` or `pause` method when one of the buttons is clicked

## Step 7 : load another video

 - Add a new button that triggers a `player.load('<xid>')` call
 - Explain how it's dynamic and does not required a full page/player reload

## Step 8 : autoplay on load

 - Add an _autoplay checkbox_
 - Get the `checked` value an send it as an extra parameter in the `player.load('<xid>', {autoplay: <value>})` call
 - A word about `autoplay` and `start`
