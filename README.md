# CC Profile Fixer

When Euro Truck Simulator 2 shows **"content change detected"** after an update, it moves every truck to a safe spot, re-attaches parked trailers and wipes the GPS route. You'd normally have to load and re-save every save, and still lose all of that.

CC Profile Fixer updates a whole profile in one go instead. You load and save **one** save in the new game version. The app reads what the update changed from that save and applies it to every save in a copy of your old profile. The game then sees saves that already match the new version, so the content change never happens: every save keeps its truck position, trailer, route and progress.

## How to use it

> [!IMPORTANT]
> **Copy your profile BEFORE you load anything in the new game version.**
> Every save that goes through "content change detected" has its trucks moved, trailers re-hooked and route wiped. The fixer works from an untouched copy of your profile, so make that copy first.

1. **Copy your outdated profile.** Close ETS2 and open `Documents\Euro Truck Simulator 2\profiles` (or `steam_profiles` if you use Steam Cloud). Copy your whole profile folder, the one with a long name of letters and numbers, somewhere safe such as your Desktop. This copy is your **outdated profile**. Don't load it in the game.
2. **Update ONE save.** Update the game and start it with your normal profile. Load any one save, accept "content change detected", then save the game. One save is all that's needed, and it doesn't matter which slot you save to.
3. **Find that updated save.** Open your profile's `save` folder (`profiles\<your profile>\save`). In File Explorer, switch to **Details** view and click the **Date modified** column so the newest is at the top. The folder at the top is the save you just made. That folder is your **updated save**.
4. **Fix the profile.** Open CC Profile Fixer and drag in:
   - the outdated profile copy from step 1, into the first box,
   - the updated save folder from step 3, into the second box,
   - a different output folder into the third box, if you don't want the default (`Desktop\CC Profile Fixer Output`),

   then click **Fix profile**. You can also click a box to browse instead. Before you start, the app shows what the update changed.

   If your profile copy is in a `.zip`, drop the `.zip` file itself and the app extracts it, or extract it yourself first. Dragging a folder out of an open zip in File Explorer doesn't work, because Windows only hands over a temporary copy of single files.
5. **Install the fixed profile.** Close ETS2. In `profiles`, replace your profile folder with the fixed one from the output folder. Keep a backup of the folder you replace.

The app shows the same steps under **How to use** in the top-right corner.

When the app starts, it checks the latest release. If the version is newer, it asks the user to download it, then restarts to install.
