# TrackmaniaGhosts
Play TMNF against your friend's ghosts

# Quickstart
1. Download and install git bash
1. [Download the game for free on steam](https://store.steampowered.com/app/11020/TrackMania_Nations_Forever/) (Its years old, so it's a pretty tiny download)
1. Launch it and check it runs. If you get a white screen [this should sort it](https://steamcommunity.com/sharedfiles/filedetails/?id=448953593).
1. Navigate to C:\Users\USERNAME\Documents\TrackMania\Tracks\Replays\ , and clone this repo
1. Create a folder in .../replays/TrackmaniaGhosts with your name (e.g.  .../replays/TrackmaniaGhosts/Scott)
1. Save the below as Update_Ghosts.sh somewhere convenient and update USER, REPO_PATH and AUTO_GHOST_PATH as appropriate. The file is set up with windows style paths for git bash.
```
USER="Your Username"
REPO_PATH="C:/Users/USERNAME/Documents/TrackMania/Tracks/Replays/TrackmaniaGhosts"
AUTO_GHOST_PATH="C:/Users/USERNAME/Documents/TrackMania/Tracks/Replays/Autosaves"

cd "$REPO_PATH"
git pull

rm -r $REPO_PATH/$USER/*
cp -r $AUTO_GHOST_PATH/* $REPO_PATH/$USER
git add .
git commit -m "$USER updated ghosts"
git push
```
