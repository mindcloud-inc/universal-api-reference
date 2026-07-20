# List Messages with MojoTxt

Retrieves messages for a MojoTxt phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/messages/list`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [List Messages](https://app.mojotxt.com/api/docs/v1/messages-list.php)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | query | `string` | no | Return only messages sent to a specific list. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
