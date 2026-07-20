# Find Adjectives For Noun with Datamuse

Finds adjectives that often describe a noun in Datamuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Adjectives For Noun](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rel_jjb` | query | `string` | yes | Noun to find commonly modifying adjectives for. |
| `topics` | query | `string` | no | Optional topic words used to rank adjective results. |
