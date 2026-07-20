# Delete Subscription List with MojoTxt

Deletes a subscription list from MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/lists/delete/:listIdOrKeyword`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Delete Subscription List](https://app.mojotxt.com/api/docs/v1/lists-delete.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listIdOrKeyword` | path | `string` | yes | The subscription list identifier or keyword value to delete. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
