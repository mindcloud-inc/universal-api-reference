# PokeAPI Core: Native API Reference

A consolidated summary of PokeAPI Core's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://pokeapi.co/docs/v2
- **API base URL:** `https://pokeapi.co/api/v2`

## Authentication

### No Authentication

PokeAPI v2 is public and does not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://pokeapi.co/docs/v2)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Ability](actions/get-ability.md) | `GET /ability/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#abilities) |
| [Get Berry](actions/get-berry.md) | `GET /berry/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#berries) |
| [Get Evolution Chain](actions/get-evolution-chain.md) | `GET /evolution-chain/[:id]/` | [docs](https://pokeapi.co/docs/v2#evolution-chains) |
| [Get Generation](actions/get-generation.md) | `GET /generation/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#generations) |
| [Get Item](actions/get-item.md) | `GET /item/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#items) |
| [Get Location](actions/get-location.md) | `GET /location/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#locations) |
| [Get Move](actions/get-move.md) | `GET /move/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#moves) |
| [Get Pokedex](actions/get-pokedex.md) | `GET /pokedex/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#pokedexes) |
| [Get Pokemon](actions/get-pokemon.md) | `GET /pokemon/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#pokemon) |
| [Get Pokemon Species](actions/get-pokemon-species.md) | `GET /pokemon-species/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#pokemon-species) |
| [Get Region](actions/get-region.md) | `GET /region/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#regions) |
| [Get Type](actions/get-type.md) | `GET /type/[:idOrName]/` | [docs](https://pokeapi.co/docs/v2#types) |
| [List Abilities](actions/list-abilities.md) | `GET /ability/` | [docs](https://pokeapi.co/docs/v2#abilities) |
| [List Berries](actions/list-berries.md) | `GET /berry/` | [docs](https://pokeapi.co/docs/v2#berries) |
| [List Evolution Chains](actions/list-evolution-chains.md) | `GET /evolution-chain/` | [docs](https://pokeapi.co/docs/v2#evolution-chains) |
| [List Generations](actions/list-generations.md) | `GET /generation/` | [docs](https://pokeapi.co/docs/v2#generations) |
| [List Items](actions/list-items.md) | `GET /item/` | [docs](https://pokeapi.co/docs/v2#items) |
| [List Locations](actions/list-locations.md) | `GET /location/` | [docs](https://pokeapi.co/docs/v2#locations) |
| [List Moves](actions/list-moves.md) | `GET /move/` | [docs](https://pokeapi.co/docs/v2#moves) |
| [List Pokedexes](actions/list-pokedexes.md) | `GET /pokedex/` | [docs](https://pokeapi.co/docs/v2#pokedexes) |
| [List Pokemon](actions/list-pokemon.md) | `GET /pokemon/` | [docs](https://pokeapi.co/docs/v2#pokemon) |
| [List Pokemon Species](actions/list-pokemon-species.md) | `GET /pokemon-species/` | [docs](https://pokeapi.co/docs/v2#pokemon-species) |
| [List Regions](actions/list-regions.md) | `GET /region/` | [docs](https://pokeapi.co/docs/v2#regions) |
| [List Types](actions/list-types.md) | `GET /type/` | [docs](https://pokeapi.co/docs/v2#types) |
