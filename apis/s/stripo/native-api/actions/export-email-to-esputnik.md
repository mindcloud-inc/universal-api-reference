# Export Email to eSputnik with Stripo

Exports an email from Stripo to eSputnik.

## Endpoint

- **Method:** `POST`
- **Path:** `/export/esputnik`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Export Email to eSputnik](https://api.stripo.email/reference/exportesputnik)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountEmail` | body | `string` | yes | Email address linked to the eSputnik account. |
| `emailId` | body | `number` | yes | Email ID to export to eSputnik. |
| `subject` | body | `string` | yes | Subject line for the exported email. |
