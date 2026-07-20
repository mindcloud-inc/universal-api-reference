# Update Subscription List with MojoTxt

Updates a subscription list in MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/lists/update/:listIdOrKeyword`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Update Subscription List](https://app.mojotxt.com/api/docs/v1/lists-update.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listIdOrKeyword` | path | `string` | yes | The subscription list identifier or keyword value to update. |
| `ListName` | body | `string` | no | The updated descriptive name of the subscription list. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `SendLastMessage` | body | `number` | no | Set to 1 to send the last sent message when someone joins the list. |
| `WelcomeMessage` | body | `string` | no | Message sent to new subscribers when they join the list. |
