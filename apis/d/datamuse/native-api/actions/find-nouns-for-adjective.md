# Find Nouns For Adjective with Datamuse

Finds nouns often described by an adjective in Datamuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Nouns For Adjective](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rel_jja` | query | `string` | yes | Adjective to find nouns it commonly modifies. |
| `topics` | query | `string` | no | Optional topic words used to rank noun results. |
