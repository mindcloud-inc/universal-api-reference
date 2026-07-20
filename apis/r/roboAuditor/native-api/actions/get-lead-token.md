# Get Lead Token with RoboAuditor

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/getToken`
- **Base URL:** `https://app.siteauditor.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | body | `number` | yes | Domain identifier (numeric). |
| `token` | body | `string` | yes | Report token value. |
| `website_url` | body | `string` | yes | Website URL associated with the lead/report token. |
