# Find Whole Terms with Datamuse

Finds parts a whole term comprises in Datamuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Find Whole Terms](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rel_com` | query | `string` | yes | Word to find whole terms that comprise it or include it as a component. |
