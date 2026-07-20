# Fetch Person Reactions with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/fetch/persons/reactions/live`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Fetch Person Reactions](https://app.reversecontact.com/docs/endpoints/live-person-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public Social profile URL whose reactions should be fetched. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for live results. |
