# List Groups For User with Faithlife

Retrieves a user's groups from Faithlife.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId/groups`
- **Base URL:** `https://accountsapi.logos.com/v2`
- **Official documentation:** [List Groups For User](https://developer.faithlife.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The Faithlife user ID or token whose groups you want to list. |
