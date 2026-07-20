# Log Event with EventLogCentral

Creates an event in EventLogCentral.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/logEvent`
- **Base URL:** `https://api.eventlogcentral.com`
- **Official documentation:** [Log Event](https://www.eventlogcentral.com/resources/api-documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | body | `string` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
| `author` | body | `string` | no |
| `category` | body | `string` | no |
| `notes` | body | `string` | no |
| `data` | body | `object` | no |
