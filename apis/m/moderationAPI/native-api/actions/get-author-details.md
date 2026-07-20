# Get Author Details with Moderation API

Retrieves author details from Moderation API.

## Endpoint

- **Method:** `GET`
- **Path:** `/authors/:id`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Get Author Details](https://docs.moderationapi.com/api-reference/author/get-author-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Either external ID or the ID assigned by moderation API. |
