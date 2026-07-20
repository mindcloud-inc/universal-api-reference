# Find Words By Spelling Pattern with Datamuse

Finds words in Datamuse by spelling pattern.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Words By Spelling Pattern](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sp` | query | `string` | yes | Spelling constraint or wildcard pattern. Use * for any number of characters and ? for one character. |
