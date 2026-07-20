# Get Group Newsfeed with Faithlife

Retrieves a group's newsfeed from Faithlife.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.faithlife.com/community/v2/groups/:groupId/newsfeed`
- **Base URL:** `https://accountsapi.logos.com/v2`
- **Official documentation:** [Get Group Newsfeed](https://developer.faithlife.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Faithlife group ID or token whose newsfeed you want to read. |
