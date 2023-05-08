# bcc-ranch

> This ranching script is a massive ranching project that allows players to own thier own ranches! With features like herding, owning animals, ranch chores, selling animals, butchering and more this script ensures that you will love tending to your virtual ranch!

# Requirements
- VORP Core
- VORP Utils
- VORP Inventory
- VORP Inputs
- bcc-utils
- VORP Character
- Menuapi

# Features
- Admin locked command to create ranches!
- Configurable chores to increase your ranches condition!
- Own 4 types of animals!
- Sell your animals with pay changing based on thier condition!
- Herd your animals around to increase thier condition the amount it increase changes based on the ranches condition!
- Custom ranch names!
- Cofigurable ranch Blips!
- Configurable Sale Locations!
- In depth webhooking!
- Version checking to help you keep upto date on new updates!
- Butcher your animals to get items from them!
- Ranch condition decreases over time when ranch owner is online!
- Highly configurable, and easy to configure!
- Easy to translate via a Config.Language!
- Inventory system built into the ranch!
- Export API for other scripts to interact with this one!

# How it works
- Admins can make a ranch by entering the command, they will be greeted with a menu to name the ranch, insert the ranches radius, and the owners static id!
- The owner will be able to walk upto where his ranch is press "G" to open a menu to manage the ranch!

# Side Notes
- Max of one ranch per character!
- After player is given one they need to relog for it too show up!
- This is a massive project there is most likely oversights if you have any suggestions or bugs report them asap!
- Ranch names can not have spaces in them currently!
- To delete ranches you will currently have to delete them manually from the database!
- Make sure to set yourself admin in the config.lua by adding your steam id where it asks for it!

## API

### Check if player owns a ranch!
- To check if a player owns a ranch you can use
```
local _source = source
local Character = VORPcore.getUser(_source).getUsedCharacter
local result = exports['bcc-ranch']:CheckIfRanchIsOwned(Character.charIdentifier)
```
- This Api Is Server Side Only result will be true if the player owns a ranch false if they do not
- You will need to pass the character id so you will have to have vorp core