# Fetch Person Comments with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/fetch/persons/comments/live`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Fetch Person Comments](https://app.reversecontact.com/docs/endpoints/live-person-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public Social profile URL whose comments should be fetched. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for live results. |
