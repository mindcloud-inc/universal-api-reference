# Add New Webhook with Filestage

Creates a new webhook in Filestage.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Add New Webhook](https://developers.filestage.io/docs/api/79twjnt5elqnk-add-new-webhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhookUrl` | body | `string` | yes |
| `events[]` | body | `array<string>` | yes |
| `headers` | body | `object` | yes |
