# VR Day 
I took my HTC vive into the office for a day of fun in VR. To help, I made this little site with information about the games I owned, so my coworkers could shop for the games they wanted to try leading up to the VR day.

The steps I took:
1. [Find my steam id](steamidfinder.com)
1. Using the Steam API to pull json data about the games I owned.
    API endpoint: `http://api.steampowered.com/IPlayerService/GetOwnedGames/v0001/?key={{api_key}}&steamid=76561197960434622&format=json&include_appinfo=1`
1. Generate Jekyll site
1. Drop data from Steam API into `_data/games.json` and remove the non-vr games from the json
1. Render game "cards" in jekyll output
1. Write a little javascript code giving me a button on each game card to invoke the steam API and spit out more game info to the javascript console
  API endpoint: `http://store.steampowered.com/api/appdetails/?appids={{appid}}`
1. Click the button for each game, copy/paste json into the games.json file.
1. Add non-steam games by hand, looking up youtube and images.
