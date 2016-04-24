### Console Commands

- **Give Player Item.** Replace ITEM with the item you want, and X with how many you want.

  `/c game.local_player.insert{name="ITEM", count=X}`
  
- **Unlock and Research all Technology.** 

  `/c game.local_player.force.research_all_technologies() `

- **Kill all biters.** This will only kill biter UNITS, not the bases or  worms. 

  `/c game.forces["enemy"].kill_all_units() `
  
- **Create ore Patch.** This will create an ore patch (Replace 'ORE' with an ore. E.G 'iron-ore', 'coal'). The richness is set by the 'amount' variable (I believe each square in the patch will have the same value). The XPOS &amp; YPOS values are how far around the player to place the ore patch. 

```
  /c  local surface = game.local_player.surface;
  for y=-YPOS, YPOS do
    for x=-XPOS, XPOS do
      surface.create_entity({name="ORE", amount=Z, position={game.local_player.position.x+x, game.local_player.position.y+y}})
    end
  end
```

