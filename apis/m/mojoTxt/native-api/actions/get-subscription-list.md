# Get Subscription List with MojoTxt

Retrieves a subscription list from MojoTxt.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/lists/get/:listIdOrKeyword`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Get Subscription List](https://app.mojotxt.com/api/docs/v1/lists-get.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listIdOrKeyword` | path | `string` | yes | The subscription list identifier or keyword value to retrieve. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
