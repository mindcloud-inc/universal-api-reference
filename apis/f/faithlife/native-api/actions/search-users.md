# Search Users with Faithlife

Finds users in Faithlife.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://accountsapi.logos.com/v2`
- **Official documentation:** [Search Users](https://developer.faithlife.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search text used to find users. |
