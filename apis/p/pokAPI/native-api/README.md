# PokéAPI: Native API Reference

A consolidated summary of PokéAPI's API configuration and 99 documented operations, with links to official documentation.

- **Official docs:** https://pokeapi.co/docs/v2
- **OpenAPI specification:** https://raw.githubusercontent.com/PokeAPI/pokeapi/master/openapi.yml
- **API base URL:** `https://pokeapi.co/api/v2`

## Authentication

### No Authentication

PokéAPI public endpoints do not require tenant credentials.

This API does not require request authentication.

[Official authentication documentation](https://pokeapi.co/docs/v2)

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (99 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Ability](actions/get-ability.md) | `GET ability/:abilityId` | [docs](https://pokeapi.co/docs/v2) |
| [Get API Meta](actions/get-api-meta.md) | `GET meta` | [docs](https://pokeapi.co/docs/v2) |
| [Get API Resources](actions/get-api-resources.md) | `GET /` | [docs](https://pokeapi.co/docs/v2) |
| [Get Berry](actions/get-berry.md) | `GET berry/:berryId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Berry Firmness](actions/get-berry-firmness.md) | `GET berry-firmness/:berryFirmnessId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Berry Flavor](actions/get-berry-flavor.md) | `GET berry-flavor/:berryFlavorId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Characteristic](actions/get-characteristic.md) | `GET characteristic/:characteristicId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Contest Effect](actions/get-contest-effect.md) | `GET contest-effect/:contestEffectId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Contest Type](actions/get-contest-type.md) | `GET contest-type/:contestTypeId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Egg Group](actions/get-egg-group.md) | `GET egg-group/:eggGroupId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Encounter Condition](actions/get-encounter-condition.md) | `GET encounter-condition/:encounterConditionId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Encounter Condition Value](actions/get-encounter-condition-value.md) | `GET encounter-condition-value/:encounterConditionValueId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Encounter Method](actions/get-encounter-method.md) | `GET encounter-method/:encounterMethodId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Evolution Chain](actions/get-evolution-chain.md) | `GET evolution-chain/:evolutionChainId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Evolution Trigger](actions/get-evolution-trigger.md) | `GET evolution-trigger/:evolutionTriggerId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Gender](actions/get-gender.md) | `GET gender/:genderId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Generation](actions/get-generation.md) | `GET generation/:generationId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Growth Rate](actions/get-growth-rate.md) | `GET growth-rate/:growthRateId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Item](actions/get-item.md) | `GET item/:itemId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Item Attribute](actions/get-item-attribute.md) | `GET item-attribute/:itemAttributeId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Item Category](actions/get-item-category.md) | `GET item-category/:itemCategoryId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Item Fling Effect](actions/get-item-fling-effect.md) | `GET item-fling-effect/:itemFlingEffectId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Item Pocket](actions/get-item-pocket.md) | `GET item-pocket/:itemPocketId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Language](actions/get-language.md) | `GET language/:languageId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Location](actions/get-location.md) | `GET location/:locationId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Location Area](actions/get-location-area.md) | `GET location-area/:locationAreaId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Machine](actions/get-machine.md) | `GET machine/:machineId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Move](actions/get-move.md) | `GET move/:moveId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Move Ailment](actions/get-move-ailment.md) | `GET move-ailment/:moveAilmentId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Move Battle Style](actions/get-move-battle-style.md) | `GET move-battle-style/:moveBattleStyleId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Move Category](actions/get-move-category.md) | `GET move-category/:moveCategoryId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Move Damage Class](actions/get-move-damage-class.md) | `GET move-damage-class/:moveDamageClassId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Move Learn Method](actions/get-move-learn-method.md) | `GET move-learn-method/:moveLearnMethodId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Move Target](actions/get-move-target.md) | `GET move-target/:moveTargetId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Nature](actions/get-nature.md) | `GET nature/:natureId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pal Park Area](actions/get-pal-park-area.md) | `GET pal-park-area/:palParkAreaId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokeathlon Stat](actions/get-pokeathlon-stat.md) | `GET pokeathlon-stat/:pokeathlonStatId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokedex](actions/get-pokedex.md) | `GET pokedex/:pokedexId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon](actions/get-pokemon.md) | `GET pokemon/:pId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Color](actions/get-pokemon-color.md) | `GET pokemon-color/:pokemonColorId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Encounters](actions/get-pokemon-encounters.md) | `GET pokemon/:pokemonId/encounters` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Form](actions/get-pokemon-form.md) | `GET pokemon-form/:pokemonFormId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Habitat](actions/get-pokemon-habitat.md) | `GET pokemon-habitat/:pokemonHabitatId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Shape](actions/get-pokemon-shape.md) | `GET pokemon-shape/:pokemonShapeId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Species](actions/get-pokemon-species.md) | `GET pokemon-species/:pokemonSpeciesId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Region](actions/get-region.md) | `GET region/:regionId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Stat](actions/get-stat.md) | `GET stat/:statId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Super Contest Effect](actions/get-super-contest-effect.md) | `GET super-contest-effect/:superContestEffectId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Type](actions/get-type.md) | `GET type/:typeId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Version](actions/get-version.md) | `GET version/:versionId` | [docs](https://pokeapi.co/docs/v2) |
| [Get Version Group](actions/get-version-group.md) | `GET version-group/:versionGroupId` | [docs](https://pokeapi.co/docs/v2) |
| [List Ability](actions/list-ability.md) | `GET ability` | [docs](https://pokeapi.co/docs/v2) |
| [List Berry](actions/list-berry.md) | `GET berry` | [docs](https://pokeapi.co/docs/v2) |
| [List Berry Firmness](actions/list-berry-firmness.md) | `GET berry-firmness` | [docs](https://pokeapi.co/docs/v2) |
| [List Berry Flavor](actions/list-berry-flavor.md) | `GET berry-flavor` | [docs](https://pokeapi.co/docs/v2) |
| [List Characteristic](actions/list-characteristic.md) | `GET characteristic` | [docs](https://pokeapi.co/docs/v2) |
| [List Contest Effect](actions/list-contest-effect.md) | `GET contest-effect` | [docs](https://pokeapi.co/docs/v2) |
| [List Contest Type](actions/list-contest-type.md) | `GET contest-type` | [docs](https://pokeapi.co/docs/v2) |
| [List Egg Group](actions/list-egg-group.md) | `GET egg-group` | [docs](https://pokeapi.co/docs/v2) |
| [List Encounter Condition](actions/list-encounter-condition.md) | `GET encounter-condition` | [docs](https://pokeapi.co/docs/v2) |
| [List Encounter Condition Value](actions/list-encounter-condition-value.md) | `GET encounter-condition-value` | [docs](https://pokeapi.co/docs/v2) |
| [List Encounter Method](actions/list-encounter-method.md) | `GET encounter-method` | [docs](https://pokeapi.co/docs/v2) |
| [List Evolution Chain](actions/list-evolution-chain.md) | `GET evolution-chain` | [docs](https://pokeapi.co/docs/v2) |
| [List Evolution Trigger](actions/list-evolution-trigger.md) | `GET evolution-trigger` | [docs](https://pokeapi.co/docs/v2) |
| [List Gender](actions/list-gender.md) | `GET gender` | [docs](https://pokeapi.co/docs/v2) |
| [List Generation](actions/list-generation.md) | `GET generation` | [docs](https://pokeapi.co/docs/v2) |
| [List Growth Rate](actions/list-growth-rate.md) | `GET growth-rate` | [docs](https://pokeapi.co/docs/v2) |
| [List Item](actions/list-item.md) | `GET item` | [docs](https://pokeapi.co/docs/v2) |
| [List Item Attribute](actions/list-item-attribute.md) | `GET item-attribute` | [docs](https://pokeapi.co/docs/v2) |
| [List Item Category](actions/list-item-category.md) | `GET item-category` | [docs](https://pokeapi.co/docs/v2) |
| [List Item Fling Effect](actions/list-item-fling-effect.md) | `GET item-fling-effect` | [docs](https://pokeapi.co/docs/v2) |
| [List Item Pocket](actions/list-item-pocket.md) | `GET item-pocket` | [docs](https://pokeapi.co/docs/v2) |
| [List Language](actions/list-language.md) | `GET language` | [docs](https://pokeapi.co/docs/v2) |
| [List Location](actions/list-location.md) | `GET location` | [docs](https://pokeapi.co/docs/v2) |
| [List Location Area](actions/list-location-area.md) | `GET location-area` | [docs](https://pokeapi.co/docs/v2) |
| [List Machine](actions/list-machine.md) | `GET machine` | [docs](https://pokeapi.co/docs/v2) |
| [List Move](actions/list-move.md) | `GET move` | [docs](https://pokeapi.co/docs/v2) |
| [List Move Ailment](actions/list-move-ailment.md) | `GET move-ailment` | [docs](https://pokeapi.co/docs/v2) |
| [List Move Battle Style](actions/list-move-battle-style.md) | `GET move-battle-style` | [docs](https://pokeapi.co/docs/v2) |
| [List Move Category](actions/list-move-category.md) | `GET move-category` | [docs](https://pokeapi.co/docs/v2) |
| [List Move Damage Class](actions/list-move-damage-class.md) | `GET move-damage-class` | [docs](https://pokeapi.co/docs/v2) |
| [List Move Learn Method](actions/list-move-learn-method.md) | `GET move-learn-method` | [docs](https://pokeapi.co/docs/v2) |
| [List Move Target](actions/list-move-target.md) | `GET move-target` | [docs](https://pokeapi.co/docs/v2) |
| [List Nature](actions/list-nature.md) | `GET nature` | [docs](https://pokeapi.co/docs/v2) |
| [List Pal Park Area](actions/list-pal-park-area.md) | `GET pal-park-area` | [docs](https://pokeapi.co/docs/v2) |
| [List Pokeathlon Stat](actions/list-pokeathlon-stat.md) | `GET pokeathlon-stat` | [docs](https://pokeapi.co/docs/v2) |
| [List Pokedex](actions/list-pokedex.md) | `GET pokedex` | [docs](https://pokeapi.co/docs/v2) |
| [List Pokemon](actions/list-pokemon.md) | `GET pokemon` | [docs](https://pokeapi.co/docs/v2) |
| [List Pokemon Color](actions/list-pokemon-color.md) | `GET pokemon-color` | [docs](https://pokeapi.co/docs/v2) |
| [List Pokemon Form](actions/list-pokemon-form.md) | `GET pokemon-form` | [docs](https://pokeapi.co/docs/v2) |
| [List Pokemon Habitat](actions/list-pokemon-habitat.md) | `GET pokemon-habitat` | [docs](https://pokeapi.co/docs/v2) |
| [List Pokemon Shape](actions/list-pokemon-shape.md) | `GET pokemon-shape` | [docs](https://pokeapi.co/docs/v2) |
| [List Pokemon Species](actions/list-pokemon-species.md) | `GET pokemon-species` | [docs](https://pokeapi.co/docs/v2) |
| [List Region](actions/list-region.md) | `GET region` | [docs](https://pokeapi.co/docs/v2) |
| [List Stat](actions/list-stat.md) | `GET stat` | [docs](https://pokeapi.co/docs/v2) |
| [List Super Contest Effect](actions/list-super-contest-effect.md) | `GET super-contest-effect` | [docs](https://pokeapi.co/docs/v2) |
| [List Type](actions/list-type.md) | `GET type` | [docs](https://pokeapi.co/docs/v2) |
| [List Version](actions/list-version.md) | `GET version` | [docs](https://pokeapi.co/docs/v2) |
| [List Version Group](actions/list-version-group.md) | `GET version-group` | [docs](https://pokeapi.co/docs/v2) |
