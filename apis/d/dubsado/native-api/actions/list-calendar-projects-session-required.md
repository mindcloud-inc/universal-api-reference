# List Calendar Projects (Session Required) with Dubsado

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/project`
- **Base URL:** `https://app.dubsado.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | yes | Start date for the calendar project window. |
| `endDate` | query | `date` | yes | End date for the calendar project window. |
| `limit` | query | `number` | no | Optional result limit observed in the Dubsado app bundle for /calendar/project reads. |
| `job` | query | `string` | no | Optional project ID filter for /calendar/project reads. |
| `client` | query | `string` | no | Optional client ID filter for /calendar/project reads. |
