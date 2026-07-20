# Update Codeless Test Alert with Headless Testing

Updates a codeless test alert in Headless Testing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lab/:id/alert`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Update Codeless Test Alert](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Alert target email, phone number, or callback URL. |
| `id` | path | `string` | yes | The codeless test identifier. |
| `kind` | body | `string` | yes | Alert delivery kind. |
| `level` | body | `string` | yes | Alert frequency level. |
