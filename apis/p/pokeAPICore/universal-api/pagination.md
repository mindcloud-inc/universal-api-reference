# PokeAPI Core Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PokeAPI Core expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/list-abilities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PokeAPI Core actions that support pagination

- [List Abilities](actions/list-abilities.md)
- [List Berries](actions/list-berries.md)
- [List Evolution Chains](actions/list-evolution-chains.md)
- [List Generations](actions/list-generations.md)
- [List Items](actions/list-items.md)
- [List Locations](actions/list-locations.md)
- [List Moves](actions/list-moves.md)
- [List Pokedexes](actions/list-pokedexes.md)
- [List Pokemon](actions/list-pokemon.md)
- [List Pokemon Species](actions/list-pokemon-species.md)
- [List Regions](actions/list-regions.md)
- [List Types](actions/list-types.md)
