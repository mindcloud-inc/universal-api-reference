# PokéAPI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PokéAPI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/list-ability?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PokéAPI actions that support pagination

- [List Ability](actions/list-ability.md)
- [List Berry](actions/list-berry.md)
- [List Berry Firmness](actions/list-berry-firmness.md)
- [List Berry Flavor](actions/list-berry-flavor.md)
- [List Characteristic](actions/list-characteristic.md)
- [List Contest Effect](actions/list-contest-effect.md)
- [List Contest Type](actions/list-contest-type.md)
- [List Egg Group](actions/list-egg-group.md)
- [List Encounter Condition](actions/list-encounter-condition.md)
- [List Encounter Condition Value](actions/list-encounter-condition-value.md)
- [List Encounter Method](actions/list-encounter-method.md)
- [List Evolution Chain](actions/list-evolution-chain.md)
- [List Evolution Trigger](actions/list-evolution-trigger.md)
- [List Gender](actions/list-gender.md)
- [List Generation](actions/list-generation.md)
- [List Growth Rate](actions/list-growth-rate.md)
- [List Item](actions/list-item.md)
- [List Item Attribute](actions/list-item-attribute.md)
- [List Item Category](actions/list-item-category.md)
- [List Item Fling Effect](actions/list-item-fling-effect.md)
- [List Item Pocket](actions/list-item-pocket.md)
- [List Language](actions/list-language.md)
- [List Location](actions/list-location.md)
- [List Location Area](actions/list-location-area.md)
- [List Machine](actions/list-machine.md)
- [List Move](actions/list-move.md)
- [List Move Ailment](actions/list-move-ailment.md)
- [List Move Battle Style](actions/list-move-battle-style.md)
- [List Move Category](actions/list-move-category.md)
- [List Move Damage Class](actions/list-move-damage-class.md)
- [List Move Learn Method](actions/list-move-learn-method.md)
- [List Move Target](actions/list-move-target.md)
- [List Nature](actions/list-nature.md)
- [List Pal Park Area](actions/list-pal-park-area.md)
- [List Pokeathlon Stat](actions/list-pokeathlon-stat.md)
- [List Pokedex](actions/list-pokedex.md)
- [List Pokemon](actions/list-pokemon.md)
- [List Pokemon Color](actions/list-pokemon-color.md)
- [List Pokemon Form](actions/list-pokemon-form.md)
- [List Pokemon Habitat](actions/list-pokemon-habitat.md)
- [List Pokemon Shape](actions/list-pokemon-shape.md)
- [List Pokemon Species](actions/list-pokemon-species.md)
- [List Region](actions/list-region.md)
- [List Stat](actions/list-stat.md)
- [List Super Contest Effect](actions/list-super-contest-effect.md)
- [List Type](actions/list-type.md)
- [List Version](actions/list-version.md)
- [List Version Group](actions/list-version-group.md)
