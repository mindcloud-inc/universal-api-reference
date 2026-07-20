# Add Shortlink to Campaign with Go4Clients

Adds shortlinks to an existing Go4Clients campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/shortlink/v1.0/{{shortlink_campaign_id}}`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Add Shortlink to Campaign](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shortlink_campaign_id` | path | `string` | yes | Shortlink campaign identifier. |
| `key[]` | body | `array<string>` | yes | List of shortlink keys to create. |
