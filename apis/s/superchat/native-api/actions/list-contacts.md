# List Contacts with Superchat

Retrieves contacts from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Contacts](https://developers.superchat.com/reference/listcontacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
