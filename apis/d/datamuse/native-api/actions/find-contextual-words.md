# Find Contextual Words with Datamuse

Finds contextual words in Datamuse by sentence context.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Contextual Words](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lc` | query | `string` | yes | Word immediately to the left of the target word in a sentence. |
| `rc` | query | `string` | no | Word immediately to the right of the target word in a sentence. |
| `sp` | query | `string` | no | Optional spelling constraint or wildcard pattern for contextual results. |
| `topics` | query | `string` | no | Optional topic words to skew results toward, with at most five words. |
