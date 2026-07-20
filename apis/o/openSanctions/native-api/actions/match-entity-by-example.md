# Match Entity By Example with OpenSanctions

## Endpoint

- **Method:** `POST`
- **Path:** `/match/:dataset`
- **Base URL:** `https://api.opensanctions.org`
- **Official documentation:** [Match Entity By Example](https://api.opensanctions.org/docs#/Matching/match_match__dataset__post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Data source or collection name to scope the match query to. Use default to match against the full OpenSanctions dataset. |
| `queries` | body | `object` | yes | Object of named entity examples to match. Each value must include schema and properties according to the EntityExample schema. |
| `threshold` | query | `number` | no | Score threshold for results to be considered matches. |
| `algorithm` | query | `string` | no | Scoring algorithm to use. The API defines best as the default algorithm. |
