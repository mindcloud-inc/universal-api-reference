# List Message History with Wbiztool

Retrieves WhatsApp message history from Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/report/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [List Message History](https://wbiztool.com/docs/history-messages-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | body | `string` | yes | Start date in DD-MM-YYYY format. |
| `end_date` | body | `string` | yes | End date in DD-MM-YYYY format. |
| `page` | body | `number` | no | Results page number. |
