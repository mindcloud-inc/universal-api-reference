# PokeAPI Word: Native API Reference

A consolidated summary of PokeAPI Word's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://pokeapi.co/docs/v2
- **API base URL:** `https://pokeapi.co/api/v2`

## Authentication

### No Authentication

PokeAPI v2 public endpoints do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://pokeapi.co/docs/v2)

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Ability](actions/get-ability.md) | `GET ability/[:abilityId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get API Resources](actions/get-api-resources.md) | `GET /` | [docs](https://pokeapi.co/docs/v2) |
| [Get Berry](actions/get-berry.md) | `GET berry/[:berryId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Egg Group](actions/get-egg-group.md) | `GET egg-group/[:eggGroupId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Evolution Chain](actions/get-evolution-chain.md) | `GET evolution-chain/[:evolutionChainId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Evolution Trigger](actions/get-evolution-trigger.md) | `GET evolution-trigger/[:evolutionTriggerId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Generation](actions/get-generation.md) | `GET generation/[:generationId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Item](actions/get-item.md) | `GET item/[:itemId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Location](actions/get-location.md) | `GET location/[:locationId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Location Area](actions/get-location-area.md) | `GET location-area/[:locationAreaId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Move](actions/get-move.md) | `GET move/[:moveId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Nature](actions/get-nature.md) | `GET nature/[:natureId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokedex](actions/get-pokedex.md) | `GET pokedex/[:pokedexId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon](actions/get-pokemon.md) | `GET pokemon/[:pokemonId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Color](actions/get-pokemon-color.md) | `GET pokemon-color/[:pokemonColorId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Encounters](actions/get-pokemon-encounters.md) | `GET pokemon/[:pokemonId]/encounters` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Form](actions/get-pokemon-form.md) | `GET pokemon-form/[:pokemonFormId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Habitat](actions/get-pokemon-habitat.md) | `GET pokemon-habitat/[:pokemonHabitatId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Pokemon Species](actions/get-pokemon-species.md) | `GET pokemon-species/[:pokemonSpeciesId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Region](actions/get-region.md) | `GET region/[:regionId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Stat](actions/get-stat.md) | `GET stat/[:statId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Type](actions/get-type.md) | `GET type/[:typeId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Version](actions/get-version.md) | `GET version/[:versionId]` | [docs](https://pokeapi.co/docs/v2) |
| [Get Version Group](actions/get-version-group.md) | `GET version-group/[:versionGroupId]` | [docs](https://pokeapi.co/docs/v2) |
