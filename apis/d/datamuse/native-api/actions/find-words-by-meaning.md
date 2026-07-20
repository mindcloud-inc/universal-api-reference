# Find Words By Meaning with Datamuse

Finds words in Datamuse by related meaning.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Words By Meaning](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ml` | query | `string` | yes | Word or phrase that the results should have a similar meaning to. |
| `topics` | query | `string` | no | Optional topic words used to rank meaning results, with at most five words. |
| `sp` | query | `string` | no | Optional spelling pattern to combine with the meaning constraint. |
