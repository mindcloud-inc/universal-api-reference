# Create Lead with Nutshell

Creates a new lead in Nutshell.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Create Lead](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leads[].description` | body | `string` | no | Description for the lead. |
| `leads[].manualValue` | body | `string` | no | Manual value to assign to the lead. |
| `leads[].dueTime.timestamp` | body | `date` | no | Due time for the lead. |
| `leads[].links.accounts[]` | body | `array<string>` | no | Company IDs to link to the lead. Send multiple values as a array. |
| `leads[].links.contacts[]` | body | `array<string>` | no | Contact IDs to link to the lead. Send multiple values as a array. |
| `leads[].links.owner` | body | `string` | no | User ID to assign as the lead owner. |
