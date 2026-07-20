# List Pushes with Pushbullet

Retrieves pushes from your Pushbullet account.

## Endpoint

- **Method:** `GET`
- **Path:** `/pushes`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [List Pushes](https://docs.pushbullet.com/v8/#pushes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modified_after` | query | `number` | no | Unix timestamp to fetch newer pushes. |
