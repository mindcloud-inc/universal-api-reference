# Create Subscription List with MojoTxt

Creates a subscription list in MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/lists/add`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Create Subscription List](https://app.mojotxt.com/api/docs/v1/lists-add.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Keyword` | body | `string` | yes | The unique keyword for the subscription list. |
| `ListName` | body | `string` | yes | The descriptive name of the subscription list. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `SendLastMessage` | body | `number` | no | Set to 1 to send the last sent message when someone joins the list. |
| `WelcomeMessage` | body | `string` | no | Message sent to new subscribers when they join the list. |
