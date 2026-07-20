# Find Frequent Followers with Datamuse

Finds words that frequently follow a given word in Datamuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Frequent Followers](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rel_bga` | query | `string` | yes | Word to find frequent followers for. |
