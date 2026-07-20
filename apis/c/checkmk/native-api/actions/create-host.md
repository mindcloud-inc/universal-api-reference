# Create Host with Checkmk

Creates a new host in Checkmk.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-types/host_config/collections/all`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Create Host](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | body | `string` | yes | Checkmk host name. |
| `folder` | body | `string` | yes | Folder slug where the host should be created. |
| `attributes` | body | `object` | yes | Host attributes object, such as ipaddress. |
