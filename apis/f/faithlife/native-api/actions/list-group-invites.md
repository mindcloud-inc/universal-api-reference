# List Group Invites with Faithlife

Retrieves a group's invites from Faithlife.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:groupId/invites`
- **Base URL:** `https://accountsapi.logos.com/v2`
- **Official documentation:** [List Group Invites](https://developer.faithlife.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Faithlife group ID or token whose invites you want to list. |
