# Steps
- Install as normal
- Navigate to `mods/aSmallCases/src/mod.ts` and remove the following text
```ts
const itemToExclude = "groovey_scavcase"; // Item to exclude
            
            for (const bot in tables.bots.types) 
            {
                // Assuming that 'types' contains the relevant information about each bot
                const botInfo = tables.bots.types[bot];
            
                // Iterate through each loot slot in the bot's inventory
                for (const lootSlot in botInfo.inventory.items) 
                {
                    // Check if the loot slot is the one you are interested in (e.g., "5783c43d2459774bbe137486")
                    if (botInfo.inventory.items[lootSlot].includes("5783c43d2459774bbe137486")) 
                    {
                        // Check if the itemID is not the excluded item
                        if (itemID !== itemToExclude) 
                        {
                            botInfo.inventory.items[lootSlot].push(itemID); 
                        }
                    }
                }
            }
```
- Navigate to `mods/aFannyPack/src/mod.ts` and remove the following text
```ts
for (const bot in tables.bots.types) 
        {
            const botInfo = tables.bots.types[bot];
            if (botInfo.inventory.equipment.Backpack["56e33680d2720be2748b4576"] != undefined)
            {
                try 
                {
                    const itemWeight = Math.round(botInfo.inventory.equipment.Backpack["56e33680d2720be2748b4576"]);
                    botInfo.inventory.equipment.Backpack[itemID] = itemWeight;
                }
                catch (error) 
                {
                    console.log(`Error adding the item ${itemID} to bot ${bot}'s tables: ${error}`);
                }
            }
        }
```


Thanks to Cryptic on the Discord for providing this info!