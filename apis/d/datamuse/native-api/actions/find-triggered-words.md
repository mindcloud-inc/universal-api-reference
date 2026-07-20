# Find Triggered Words with Datamuse

Finds words in Datamuse strongly associated with a given word.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Triggered Words](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rel_trg` | query | `string` | yes | Word to find statistically associated triggered words for. |
