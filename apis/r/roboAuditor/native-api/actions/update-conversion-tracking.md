# Update Conversion Tracking with RoboAuditor

## Endpoint

- **Method:** `POST`
- **Path:** `/integrations/conversion-tracking`
- **Base URL:** `https://app.siteauditor.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `analytics_script` | body | `string` | no | HTML/JavaScript conversion tracking snippet. |
| `view_analytics` | body | `number` | no | Enable conversion tracking (1 or 0). |
