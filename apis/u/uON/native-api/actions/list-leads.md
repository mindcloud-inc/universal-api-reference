# List Leads with U-ON

Retrieves lead records stored in U-ON.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/{date_from}/{date_to}/{page}.json`
- **Base URL:** `https://api.u-on.ru/{key}`
- **Official documentation:** [List Leads](https://api.u-on.travel/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | path | `date` | yes | date_from path parameter |
| `date_to` | path | `date` | yes | date_to path parameter |
