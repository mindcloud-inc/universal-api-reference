# List Phone Number Subscribers with MojoTxt

Retrieves subscribers for a MojoTxt phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/subscribers/list`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [List Phone Number Subscribers](https://app.mojotxt.com/api/docs/v1/subscribers-list.php)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | query | `string` | no | Return only subscribers from a specific subscription list. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
