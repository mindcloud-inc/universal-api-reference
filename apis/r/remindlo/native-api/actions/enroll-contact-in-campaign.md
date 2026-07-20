# Enroll Contact In Campaign with Remindlo

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns-enroll`
- **Base URL:** `https://api.remindlo.co.uk/v1`
- **Official documentation:** [Enroll Contact In Campaign](https://www.remindlo.co.uk/help/sms-reminder-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes |
| `contact_id` | body | `string` | no |
| `customer_id` | body | `string` | no |
