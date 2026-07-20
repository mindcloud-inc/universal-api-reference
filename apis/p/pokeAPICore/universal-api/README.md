# <img src="https://images.mindcloud.co/apps/icons/500px-poke-ball-icon_1777905434331.png" alt="PokeAPI Core logo" width="28" height="28"> PokeAPI Core: Universal API

Access the public PokeAPI v2 catalog of Pokemon, species, abilities, types, moves, items, berries, evolution chains, generations, Pokedexes, regions, and locations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pokeAPICore/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pokeapi.co/
- **Vendor API docs:** https://pokeapi.co/docs/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Ability](actions/get-ability.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-ability?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Ability

| Action | Method | Description |
| --- | --- | --- |
| [Get Ability](actions/get-ability.md) | GET | Retrieves an ability from PokeAPI Core. |
| [List Abilities](actions/list-abilities.md) | GET | Retrieves a page of abilities from PokeAPI Core. |

### Berry

| Action | Method | Description |
| --- | --- | --- |
| [Get Berry](actions/get-berry.md) | GET | Retrieves a berry from PokeAPI Core. |
| [List Berries](actions/list-berries.md) | GET | Retrieves a page of berries from PokeAPI Core. |

### Evolution Chain

| Action | Method | Description |
| --- | --- | --- |
| [Get Evolution Chain](actions/get-evolution-chain.md) | GET | Retrieves an evolution chain from PokeAPI Core. |
| [List Evolution Chains](actions/list-evolution-chains.md) | GET | Retrieves a page of evolution chains from PokeAPI Core. |

### Generation

| Action | Method | Description |
| --- | --- | --- |
| [Get Generation](actions/get-generation.md) | GET | Retrieves a generation from PokeAPI Core. |
| [List Generations](actions/list-generations.md) | GET | Retrieves a page of generations from PokeAPI Core. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from PokeAPI Core. |
| [List Items](actions/list-items.md) | GET | Retrieves a page of items from PokeAPI Core. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from PokeAPI Core. |
| [List Locations](actions/list-locations.md) | GET | Retrieves a page of locations from PokeAPI Core. |

### Move

| Action | Method | Description |
| --- | --- | --- |
| [Get Move](actions/get-move.md) | GET | Retrieves a move from PokeAPI Core. |
| [List Moves](actions/list-moves.md) | GET | Retrieves a page of moves from PokeAPI Core. |

### Pokedex

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokedex](actions/get-pokedex.md) | GET | Retrieves a Pokedex from PokeAPI Core. |
| [List Pokedexes](actions/list-pokedexes.md) | GET | Retrieves a page of Pokedexes from PokeAPI Core. |

### Pokemon

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon](actions/get-pokemon.md) | GET | Retrieves a Pokemon from PokeAPI Core. |
| [List Pokemon](actions/list-pokemon.md) | GET | Retrieves a page of Pokemon from PokeAPI Core. |

### Pokemon Species

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Species](actions/get-pokemon-species.md) | GET | Retrieves a Pokemon species from PokeAPI Core. |
| [List Pokemon Species](actions/list-pokemon-species.md) | GET | Retrieves a page of Pokemon species from PokeAPI Core. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [Get Region](actions/get-region.md) | GET | Retrieves a region from PokeAPI Core. |
| [List Regions](actions/list-regions.md) | GET | Retrieves a page of regions from PokeAPI Core. |

### Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Type](actions/get-type.md) | GET | Retrieves a type from PokeAPI Core. |
| [List Types](actions/list-types.md) | GET | Retrieves a page of types from PokeAPI Core. |

