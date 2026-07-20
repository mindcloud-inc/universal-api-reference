# Update Record with Rubitime

Updates an existing record in Rubitime.

## Endpoint

- **Method:** `POST`
- **Path:** `/update-record`
- **Base URL:** `https://rubitime.ru/api2`
- **Official documentation:** [Update Record](https://rubitime.ru/faq/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Rubitime record ID to update. |
| `branch_id` | body | `number` | no | Rubitime branch ID. |
| `cooperator_id` | body | `number` | no | Rubitime employee/cooperator ID. |
| `service_id` | body | `number` | no | Rubitime service ID. |
| `record` | body | `string` | no | Appointment date and time. |
| `status` | body | `number` | no | Record status code documented by Rubitime. |
| `name` | body | `string` | no | Customer full name. |
| `email` | body | `string` | no | Customer email address. |
| `phone` | body | `string` | no | Customer phone number. |
| `comment` | body | `string` | no | Customer comment for the record. |
| `price` | body | `number` | no | Service price. |
| `duration` | body | `number` | no | Service duration in minutes. |
| `prepayment` | body | `number` | no | Prepayment amount. |
| `prepayment_date` | body | `string` | no | Prepayment completion date and time. |
| `prepayment_url` | body | `string` | no | Prepayment URL. |
| `reminder_minutes` | body | `number` | no | Reminder offset in minutes. |
| `reminder` | body | `string` | no | Optional reminder timestamp documented by Rubitime. |
| `whom` | body | `number` | no | Creator marker; 0 means customer, other values indicate administrator. |
| `source` | body | `string` | no | Record source. |
| `custom_field1` | body | `string` | no | First Rubitime custom field value. |
