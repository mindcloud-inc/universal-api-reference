# <img src="https://images.mindcloud.co/apps/icons/pok-api_1776177965785.png" alt="PokéAPI logo" width="28" height="28"> PokéAPI: Universal API

Public REST wrapper for PokéAPI v2, covering the full public Pokémon resource catalog for read-only lookup and listing workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pokAPI/latest
- **Actions:** 99
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pokeapi.co/
- **Vendor API docs:** https://pokeapi.co/docs/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pokemon](actions/list-pokemon.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/list-pokemon?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (99)

### Ability

| Action | Method | Description |
| --- | --- | --- |
| [Get Ability](actions/get-ability.md) | GET | Retrieves details for an ability from PokéAPI. |
| [List Ability](actions/list-ability.md) | GET | Retrieves abilities from PokéAPI. |

### Api Meta

| Action | Method | Description |
| --- | --- | --- |
| [Get API Meta](actions/get-api-meta.md) | GET | Retrieves PokéAPI deployment metadata. |

### Api Resources

| Action | Method | Description |
| --- | --- | --- |
| [Get API Resources](actions/get-api-resources.md) | GET | Retrieves PokéAPI resource endpoints. |

### Berry

| Action | Method | Description |
| --- | --- | --- |
| [Get Berry](actions/get-berry.md) | GET | Retrieves details for a berry from PokéAPI. |
| [List Berry](actions/list-berry.md) | GET | Retrieves berries from PokéAPI. |

### Berry Firmness

| Action | Method | Description |
| --- | --- | --- |
| [Get Berry Firmness](actions/get-berry-firmness.md) | GET | Retrieves details for a berry firmness from PokéAPI. |
| [List Berry Firmness](actions/list-berry-firmness.md) | GET | Retrieves berry firmnesses from PokéAPI. |

### Berry Flavor

| Action | Method | Description |
| --- | --- | --- |
| [Get Berry Flavor](actions/get-berry-flavor.md) | GET | Retrieves details for a berry flavor from PokéAPI. |
| [List Berry Flavor](actions/list-berry-flavor.md) | GET | Retrieves berry flavors from PokéAPI. |

### Characteristic

| Action | Method | Description |
| --- | --- | --- |
| [Get Characteristic](actions/get-characteristic.md) | GET | Retrieves details for a characteristic from PokéAPI. |
| [List Characteristic](actions/list-characteristic.md) | GET | Retrieves characteristics from PokéAPI. |

### Contest Effect

| Action | Method | Description |
| --- | --- | --- |
| [Get Contest Effect](actions/get-contest-effect.md) | GET | Retrieves details for a contest effect from PokéAPI. |
| [List Contest Effect](actions/list-contest-effect.md) | GET | Retrieves contest effects from PokéAPI. |

### Contest Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Contest Type](actions/get-contest-type.md) | GET | Retrieves details for a contest type from PokéAPI. |
| [List Contest Type](actions/list-contest-type.md) | GET | Retrieves contest types from PokéAPI. |

### Egg Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Egg Group](actions/get-egg-group.md) | GET | Retrieves details for an egg group from PokéAPI. |
| [List Egg Group](actions/list-egg-group.md) | GET | Retrieves egg groups from PokéAPI. |

### Encounter Condition

| Action | Method | Description |
| --- | --- | --- |
| [Get Encounter Condition](actions/get-encounter-condition.md) | GET | Retrieves details for an encounter condition from PokéAPI. |
| [List Encounter Condition](actions/list-encounter-condition.md) | GET | Retrieves encounter conditions from PokéAPI. |

### Encounter Condition Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Encounter Condition Value](actions/get-encounter-condition-value.md) | GET | Retrieves details for an encounter condition value from PokéAPI. |
| [List Encounter Condition Value](actions/list-encounter-condition-value.md) | GET | Retrieves encounter condition values from PokéAPI. |

### Encounter Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Encounter Method](actions/get-encounter-method.md) | GET | Retrieves details for an encounter method from PokéAPI. |
| [List Encounter Method](actions/list-encounter-method.md) | GET | Retrieves encounter methods from PokéAPI. |

### Evolution Chain

| Action | Method | Description |
| --- | --- | --- |
| [Get Evolution Chain](actions/get-evolution-chain.md) | GET | Retrieves details for an evolution chain from PokéAPI. |
| [List Evolution Chain](actions/list-evolution-chain.md) | GET | Retrieves evolution chains from PokéAPI. |

### Evolution Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Get Evolution Trigger](actions/get-evolution-trigger.md) | GET | Retrieves details for an evolution trigger from PokéAPI. |
| [List Evolution Trigger](actions/list-evolution-trigger.md) | GET | Retrieves evolution triggers from PokéAPI. |

### Gender

| Action | Method | Description |
| --- | --- | --- |
| [Get Gender](actions/get-gender.md) | GET | Retrieves details for a gender from PokéAPI. |
| [List Gender](actions/list-gender.md) | GET | Retrieves genders from PokéAPI. |

### Generation

| Action | Method | Description |
| --- | --- | --- |
| [Get Generation](actions/get-generation.md) | GET | Retrieves details for a generation from PokéAPI. |
| [List Generation](actions/list-generation.md) | GET | Retrieves generations from PokéAPI. |

### Growth Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Growth Rate](actions/get-growth-rate.md) | GET | Retrieves details for a growth rate from PokéAPI. |
| [List Growth Rate](actions/list-growth-rate.md) | GET | Retrieves growth rates from PokéAPI. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves details for an item from PokéAPI. |
| [List Item](actions/list-item.md) | GET | Retrieves items from PokéAPI. |

### Item Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Attribute](actions/get-item-attribute.md) | GET | Retrieves details for an item attribute from PokéAPI. |
| [List Item Attribute](actions/list-item-attribute.md) | GET | Retrieves item attributes from PokéAPI. |

### Item Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Category](actions/get-item-category.md) | GET | Retrieves details for an item category from PokéAPI. |
| [List Item Category](actions/list-item-category.md) | GET | Retrieves item categories from PokéAPI. |

### Item Fling Effect

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Fling Effect](actions/get-item-fling-effect.md) | GET | Retrieves details for an item fling effect from PokéAPI. |
| [List Item Fling Effect](actions/list-item-fling-effect.md) | GET | Retrieves item fling effects from PokéAPI. |

### Item Pocket

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Pocket](actions/get-item-pocket.md) | GET | Retrieves details for an item pocket from PokéAPI. |
| [List Item Pocket](actions/list-item-pocket.md) | GET | Retrieves item pockets from PokéAPI. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Get Language](actions/get-language.md) | GET | Retrieves details for a language from PokéAPI. |
| [List Language](actions/list-language.md) | GET | Retrieves languages from PokéAPI. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves details for a location from PokéAPI. |
| [List Location](actions/list-location.md) | GET | Retrieves locations from PokéAPI. |

### Location Area

| Action | Method | Description |
| --- | --- | --- |
| [Get Location Area](actions/get-location-area.md) | GET | Retrieves details for a location area from PokéAPI. |
| [List Location Area](actions/list-location-area.md) | GET | Retrieves location areas from PokéAPI. |

### Machine

| Action | Method | Description |
| --- | --- | --- |
| [Get Machine](actions/get-machine.md) | GET | Retrieves details for a machine from PokéAPI. |
| [List Machine](actions/list-machine.md) | GET | Retrieves machines from PokéAPI. |

### Move

| Action | Method | Description |
| --- | --- | --- |
| [Get Move](actions/get-move.md) | GET | Retrieves details for a move from PokéAPI. |
| [List Move](actions/list-move.md) | GET | Retrieves moves from PokéAPI. |

### Move Ailment

| Action | Method | Description |
| --- | --- | --- |
| [Get Move Ailment](actions/get-move-ailment.md) | GET | Retrieves details for a move ailment from PokéAPI. |
| [List Move Ailment](actions/list-move-ailment.md) | GET | Retrieves move ailments from PokéAPI. |

### Move Battle Style

| Action | Method | Description |
| --- | --- | --- |
| [Get Move Battle Style](actions/get-move-battle-style.md) | GET | Retrieves details for a move battle style from PokéAPI. |
| [List Move Battle Style](actions/list-move-battle-style.md) | GET | Retrieves move battle styles from PokéAPI. |

### Move Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Move Category](actions/get-move-category.md) | GET | Retrieves details for a move category from PokéAPI. |
| [List Move Category](actions/list-move-category.md) | GET | Retrieves move categories from PokéAPI. |

### Move Damage Class

| Action | Method | Description |
| --- | --- | --- |
| [Get Move Damage Class](actions/get-move-damage-class.md) | GET | Retrieves details for a move damage class from PokéAPI. |
| [List Move Damage Class](actions/list-move-damage-class.md) | GET | Retrieves move damage classes from PokéAPI. |

### Move Learn Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Move Learn Method](actions/get-move-learn-method.md) | GET | Retrieves details for a move learn method from PokéAPI. |
| [List Move Learn Method](actions/list-move-learn-method.md) | GET | Retrieves move learn methods from PokéAPI. |

### Move Target

| Action | Method | Description |
| --- | --- | --- |
| [Get Move Target](actions/get-move-target.md) | GET | Retrieves details for a move target from PokéAPI. |
| [List Move Target](actions/list-move-target.md) | GET | Retrieves move targets from PokéAPI. |

### Nature

| Action | Method | Description |
| --- | --- | --- |
| [Get Nature](actions/get-nature.md) | GET | Retrieves details for a nature from PokéAPI. |
| [List Nature](actions/list-nature.md) | GET | Retrieves natures from PokéAPI. |

### Pal Park Area

| Action | Method | Description |
| --- | --- | --- |
| [Get Pal Park Area](actions/get-pal-park-area.md) | GET | Retrieves details for a pal park area from PokéAPI. |
| [List Pal Park Area](actions/list-pal-park-area.md) | GET | Retrieves pal park areas from PokéAPI. |

### Pokeathlon Stat

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokeathlon Stat](actions/get-pokeathlon-stat.md) | GET | Retrieves details for a pokeathlon stat from PokéAPI. |
| [List Pokeathlon Stat](actions/list-pokeathlon-stat.md) | GET | Retrieves pokeathlon stats from PokéAPI. |

### Pokedex

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokedex](actions/get-pokedex.md) | GET | Retrieves details for a pokedex from PokéAPI. |
| [List Pokedex](actions/list-pokedex.md) | GET | Retrieves pokedexes from PokéAPI. |

### Pokemon

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon](actions/get-pokemon.md) | GET | Retrieves details for a pokemon from PokéAPI. |
| [List Pokemon](actions/list-pokemon.md) | GET | Retrieves pokemon from PokéAPI. |

### Pokemon Color

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Color](actions/get-pokemon-color.md) | GET | Retrieves details for a pokemon color from PokéAPI. |
| [List Pokemon Color](actions/list-pokemon-color.md) | GET | Retrieves pokemon colors from PokéAPI. |

### Pokemon Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Form](actions/get-pokemon-form.md) | GET | Retrieves details for a pokemon form from PokéAPI. |
| [List Pokemon Form](actions/list-pokemon-form.md) | GET | Retrieves pokemon forms from PokéAPI. |

### Pokemon Habitat

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Habitat](actions/get-pokemon-habitat.md) | GET | Retrieves details for a pokemon habitat from PokéAPI. |
| [List Pokemon Habitat](actions/list-pokemon-habitat.md) | GET | Retrieves pokemon habitats from PokéAPI. |

### Pokemon Shape

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Shape](actions/get-pokemon-shape.md) | GET | Retrieves details for a pokemon shape from PokéAPI. |
| [List Pokemon Shape](actions/list-pokemon-shape.md) | GET | Retrieves pokemon shapes from PokéAPI. |

### Pokemon Species

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Species](actions/get-pokemon-species.md) | GET | Retrieves details for a pokemon species from PokéAPI. |
| [List Pokemon Species](actions/list-pokemon-species.md) | GET | Retrieves pokemon species from PokéAPI. |

### Pokemonencounterlocationarea

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Encounters](actions/get-pokemon-encounters.md) | GET | Retrieves pokemon encounter locations from PokéAPI. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [Get Region](actions/get-region.md) | GET | Retrieves details for a region from PokéAPI. |
| [List Region](actions/list-region.md) | GET | Retrieves regions from PokéAPI. |

### Stat

| Action | Method | Description |
| --- | --- | --- |
| [Get Stat](actions/get-stat.md) | GET | Retrieves details for a stat from PokéAPI. |
| [List Stat](actions/list-stat.md) | GET | Retrieves stats from PokéAPI. |

### Super Contest Effect

| Action | Method | Description |
| --- | --- | --- |
| [Get Super Contest Effect](actions/get-super-contest-effect.md) | GET | Retrieves details for a super contest effect from PokéAPI. |
| [List Super Contest Effect](actions/list-super-contest-effect.md) | GET | Retrieves super contest effects from PokéAPI. |

### Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Type](actions/get-type.md) | GET | Retrieves details for a type from PokéAPI. |
| [List Type](actions/list-type.md) | GET | Retrieves types from PokéAPI. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Version](actions/get-version.md) | GET | Retrieves details for a version from PokéAPI. |
| [List Version](actions/list-version.md) | GET | Retrieves versions from PokéAPI. |

### Version Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Version Group](actions/get-version-group.md) | GET | Retrieves details for a version group from PokéAPI. |
| [List Version Group](actions/list-version-group.md) | GET | Retrieves version groups from PokéAPI. |

