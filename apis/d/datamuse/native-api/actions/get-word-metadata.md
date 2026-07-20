# Get Word Metadata with Datamuse

Retrieves Datamuse metadata for a word by exact spelling.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Get Word Metadata](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sp` | query | `string` | yes | Word to look up metadata for. |
| `md` | query | `string` | no | Metadata flags to include. Datamuse supports d, p, s, r, and f. |
