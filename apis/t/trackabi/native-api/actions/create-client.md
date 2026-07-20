# Create Client with Trackabi

Creates a new client in Trackabi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/clients`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [Create Client](https://trackabi.com/help/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The client's name. |
| `short_name` | body | `string` | no | Short name of the client. |
| `contact_person` | body | `string` | no | Contact person. |
| `address` | body | `string` | no | Address of the client. |
| `email` | body | `string` | no | Client's email. |
| `phone` | body | `string` | no | Client's phone number. |
| `notes` | body | `string` | no | Additional notes about the client. |
| `currency` | body | `string` | no | Client's currency. |
| `hourly_rate` | body | `number` | no | Hourly rate. |
| `cost_hourly_rate` | body | `number` | no | Cost hourly rate. |
