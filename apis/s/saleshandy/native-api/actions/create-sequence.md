# Create Sequence with Saleshandy

## Endpoint

- **Method:** `POST`
- **Path:** `/sequences`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [Create Sequence](https://developer.saleshandy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the sequence to create. |
| `emailAccountId` | body | `string` | no | Optional hashed ID of the email account to attach to the sequence. |
| `scheduleId` | body | `string` | no | Optional hashed ID of the schedule to assign to the sequence. |
