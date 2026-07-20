# Create webhook with AiWifi

Creates a new webhook configuration in AiWifi.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/{{brandId}}/webhook-configs`
- **Base URL:** `https://api.aiwifi.io/api/v1`
- **Official documentation:** [Create webhook](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `url` | body | `string` | yes | — |
| `allEvents` | body | `boolean` | yes | — |
| `eventCodes` | body | `list<string>` | no | Accepted values: `guest.connected`, `guest.data`, `guest.interests`, `surveyAnswer.created`. Send multiple values as a array. |
