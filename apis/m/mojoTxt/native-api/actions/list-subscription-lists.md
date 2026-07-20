# List Subscription Lists with MojoTxt

Retrieves subscription lists from MojoTxt.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/lists/list`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [List Subscription Lists](https://app.mojotxt.com/api/docs/v1/lists-list.php)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `Stats` | query | `string` | no | Set to 1 to include subscription list statistics in the response. |
