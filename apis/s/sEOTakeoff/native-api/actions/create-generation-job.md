# Create Generation Job with SEOTakeoff

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/generate`
- **Base URL:** `https://api.seotakeoff.com`
- **Official documentation:** [Create Generation Job](https://api.seotakeoff.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | body | `string` | yes | Tenant slug, like mindcloud-co. |
| `headline` | body | `string` | yes | Article headline. |
| `keyword` | body | `string` | yes | Target SEO keyword. |
| `cluster` | body | `string` | yes | Content cluster name. |
| `headline_id` | body | `string` | no | Optional queue item or headline ID for tracking. |
| `language` | body | `string` | no | Optional ISO language code. |
