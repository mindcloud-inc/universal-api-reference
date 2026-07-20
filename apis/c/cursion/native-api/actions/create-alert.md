# Create Alert with Cursion

## Endpoint

- **Method:** `POST`
- **Path:** `/alert`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Create Alert](https://docs.cursion.dev/api/alert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actions` | body | `list<object>` | yes | The list of alert action objects. |
| `expressions` | body | `list<object>` | yes | The list of alert expression objects. |
| `name` | body | `string` | yes | The alert display name. |
| `schedule_id` | body | `string` | no | The optional schedule to attach this alert to. |
| `site_id` | body | `string` | yes | The site identifier for the alert. |
