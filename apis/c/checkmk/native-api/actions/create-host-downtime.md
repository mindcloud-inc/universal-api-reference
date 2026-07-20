# Create Host Downtime with Checkmk

Creates a host-related scheduled downtime in Checkmk.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-types/downtime/collections/host`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Create Host Downtime](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/downtime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | body | `string` | yes | Host to schedule downtime for. |
| `comment` | body | `string` | yes | Downtime comment. |
| `start_time` | body | `date` | yes | Downtime start time. |
| `end_time` | body | `date` | yes | Downtime end time. |
