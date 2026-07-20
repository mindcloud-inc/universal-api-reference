# <img src="https://images.mindcloud.co/apps/icons/poke-apiword_1777904999359.png" alt="PokeAPI Word logo" width="28" height="28"> PokeAPI Word: Universal API

Public REST wrapper for PokeAPI v2, covering read-only Pokemon lookup and catalog workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pokeAPIWord/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pokeapi.co/
- **Vendor API docs:** https://pokeapi.co/docs/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Ability](actions/get-ability.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-ability?connectionId=$CONNECTION_ID&abilityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Ability

| Action | Method | Description |
| --- | --- | --- |
| [Get Ability](actions/get-ability.md) | GET | Retrieves details for an ability from PokeAPI. |

### Api Resources

| Action | Method | Description |
| --- | --- | --- |
| [Get API Resources](actions/get-api-resources.md) | GET | Retrieves available API resources from PokeAPI. |

### Berry

| Action | Method | Description |
| --- | --- | --- |
| [Get Berry](actions/get-berry.md) | GET | Retrieves details for a berry from PokeAPI. |

### Egg Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Egg Group](actions/get-egg-group.md) | GET | Retrieves egg group details from PokeAPI. |

### Evolution Chain

| Action | Method | Description |
| --- | --- | --- |
| [Get Evolution Chain](actions/get-evolution-chain.md) | GET | Retrieves evolution chain details from PokeAPI. |

### Evolution Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Get Evolution Trigger](actions/get-evolution-trigger.md) | GET | Retrieves evolution trigger details from PokeAPI. |

### Generation

| Action | Method | Description |
| --- | --- | --- |
| [Get Generation](actions/get-generation.md) | GET | Retrieves details for a generation from PokeAPI. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves details for an item from PokeAPI. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves details for a location from PokeAPI. |

### Location Area

| Action | Method | Description |
| --- | --- | --- |
| [Get Location Area](actions/get-location-area.md) | GET | Retrieves location area details from PokeAPI. |

### Move

| Action | Method | Description |
| --- | --- | --- |
| [Get Move](actions/get-move.md) | GET | Retrieves details for a move from PokeAPI. |

### Nature

| Action | Method | Description |
| --- | --- | --- |
| [Get Nature](actions/get-nature.md) | GET | Retrieves details for a nature from PokeAPI. |

### Pokedex

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokedex](actions/get-pokedex.md) | GET | Retrieves details for a Pokedex from PokeAPI. |

### Pokemon

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon](actions/get-pokemon.md) | GET | Retrieves details for a Pokemon from PokeAPI. |

### Pokemon Color

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Color](actions/get-pokemon-color.md) | GET | Retrieves Pokemon color details from PokeAPI. |

### Pokemon Encounter Location Area

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Encounters](actions/get-pokemon-encounters.md) | GET | Retrieves Pokemon encounter locations from PokeAPI. |

### Pokemon Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Form](actions/get-pokemon-form.md) | GET | Retrieves Pokemon form details from PokeAPI. |

### Pokemon Habitat

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Habitat](actions/get-pokemon-habitat.md) | GET | Retrieves Pokemon habitat details from PokeAPI. |

### Pokemon Species

| Action | Method | Description |
| --- | --- | --- |
| [Get Pokemon Species](actions/get-pokemon-species.md) | GET | Retrieves Pokemon species details from PokeAPI. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [Get Region](actions/get-region.md) | GET | Retrieves details for a region from PokeAPI. |

### Stat

| Action | Method | Description |
| --- | --- | --- |
| [Get Stat](actions/get-stat.md) | GET | Retrieves details for a stat from PokeAPI. |

### Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Type](actions/get-type.md) | GET | Retrieves details for a type from PokeAPI. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Version](actions/get-version.md) | GET | Retrieves details for a version from PokeAPI. |

### Version Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Version Group](actions/get-version-group.md) | GET | Retrieves version group details from PokeAPI. |

