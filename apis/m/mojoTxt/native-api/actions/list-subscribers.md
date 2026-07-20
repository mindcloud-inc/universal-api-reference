# List Subscribers with MojoTxt

Retrieves subscribers from MojoTxt.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/list`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [List Subscribers](https://app.mojotxt.com/api/docs/v1/subscribers-list.php)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EmailKnown` | query | `string` | no | Set to 1 to return only subscribers with known email addresses. |
| `ListID` | query | `string` | no | Return only subscribers from a specific subscription list. |
| `NameKnown` | query | `string` | no | Set to 1 to return only subscribers with known first names. |
