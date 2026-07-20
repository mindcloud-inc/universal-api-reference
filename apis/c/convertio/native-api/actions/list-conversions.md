# List Conversions with Convertio

Retrieves conversions and statuses from Convertio.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/list`
- **Base URL:** `https://api.convertio.co`
- **Official documentation:** [List Conversions](https://developers.convertio.co/api/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `number` | no | Number of latest conversion records to return. |
| `status` | body | `string` | no | Filter by conversion status. |
