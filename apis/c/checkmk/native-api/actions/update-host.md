# Update Host with Checkmk

Updates an existing host in Checkmk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/objects/host_config/{host_name}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Update Host](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | path | `string` | yes | Checkmk host name. |
| `update_attributes` | body | `object` | no | Attributes to update. |
| `remove_attributes[]` | body | `array<string>` | no | Attribute names to remove. |
