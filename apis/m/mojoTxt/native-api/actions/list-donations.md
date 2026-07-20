# List Donations with MojoTxt

Retrieves donations for a MojoTxt phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/donations/list`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [List Donations](https://app.mojotxt.com/api/docs/v1/donations-list.php)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `Stats` | query | `string` | no | Set to 1 to include donation statistics in the response. |
