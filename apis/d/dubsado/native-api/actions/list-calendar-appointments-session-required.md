# List Calendar Appointments (Session Required) with Dubsado

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/appointment`
- **Base URL:** `https://app.dubsado.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | yes | Start date for the calendar appointment window. |
| `endDate` | query | `date` | yes | End date for the calendar appointment window. |
| `limit` | query | `number` | no | Optional result limit observed in the Dubsado app bundle for /calendar/appointment reads. |
| `job` | query | `string` | no | Optional project ID filter for /calendar/appointment reads. |
| `client` | query | `string` | no | Optional client ID filter for /calendar/appointment reads. |
