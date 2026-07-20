# Find More Specific Words with Datamuse

Finds more specific words in Datamuse for a given word.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find More Specific Words](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rel_gen` | query | `string` | yes | Word to find more specific direct hyponyms for. |
