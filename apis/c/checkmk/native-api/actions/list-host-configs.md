# List Host Configs with Checkmk

Retrieves host configuration records from Checkmk.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain-types/host_config/collections/all`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [List Host Configs](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `effective_attributes` | query | `boolean` | no | Include effective host attributes. |
