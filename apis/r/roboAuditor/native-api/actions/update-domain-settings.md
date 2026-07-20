# Update Domain Settings with RoboAuditor

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-settings/`
- **Base URL:** `https://app.siteauditor.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `white_label_url` | body | `string` | yes | Custom domain URL to bind. |
| `is_cname_valid` | body | `boolean` | no | Whether DNS CNAME is validated. |
