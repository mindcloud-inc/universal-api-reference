# Merge Idea with Canny

Merges an idea into another idea in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ideas/merge`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Merge Idea](https://developers.canny.io/api-reference#merge_idea)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mergeIdeaID` | body | `string` | yes | The idea unique identifier that will be merged. |
| `intoIdeaID` | body | `string` | yes | The idea unique identifier that the merge idea will be merged into. |
| `mergerID` | body | `string` | yes | The unique identifier of the user performing the merge. |
