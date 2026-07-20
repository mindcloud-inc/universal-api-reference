# Retrieve Idea with Canny

Retrieves a single idea from Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ideas/retrieve`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Retrieve Idea](https://developers.canny.io/api-reference#retrieve_idea)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | The idea unique identifier. |
| `urlName` | body | `string` | no | The idea unique URL name. |
