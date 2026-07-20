# Find Kind Of Words with Datamuse

Finds what a word is a kind of in Datamuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Kind Of Words](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rel_spc` | query | `string` | yes | Word to find direct hypernyms or broader kind-of terms for. |
