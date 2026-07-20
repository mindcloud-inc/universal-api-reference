# Count Domain Emails with Hunter

## Endpoint

- **Method:** `GET`
- **Path:** `/email-count`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Count Domain Emails](https://hunter.io/api-documentation/v2#email-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Company domain to count emails for. |
| `company` | query | `string` | no | — |
| `type` | query | `string` | no | — |
