# Find Frequent Predecessors with Datamuse

Finds words that frequently precede a given word in Datamuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Frequent Predecessors](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rel_bgb` | query | `string` | yes | Word to find frequent predecessors for. |
