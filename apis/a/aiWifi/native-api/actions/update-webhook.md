# Update webhook with AiWifi

Updates an existing webhook configuration in AiWifi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/brands/{{brandId}}/webhook-configs/{{webhookId}}`
- **Base URL:** `https://api.aiwifi.io/api/v1`
- **Official documentation:** [Update webhook](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `number` | yes | — |
| `name` | body | `string` | yes | — |
| `url` | body | `string` | yes | — |
| `allEvents` | body | `boolean` | yes | — |
| `eventCodes` | body | `list<string>` | no | Accepted values: `guest.connected`, `guest.data`, `guest.interests`, `surveyAnswer.created`. Send multiple values as a array. |
