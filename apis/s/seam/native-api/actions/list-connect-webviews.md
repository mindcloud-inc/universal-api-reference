# List Connect Webviews with Seam

Retrieves a list of connect webviews from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/connect_webviews/list`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [List Connect Webviews](https://docs.seam.co/latest/api/connect_webviews/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_key` | body | `string` | no | Customer key for which you want to list connect webviews. |
| `search` | body | `string` | no | Search string for connect webviews. |
| `user_identifier_key` | body | `string` | no | Your user ID for the user by which you want to filter connect webviews. |
