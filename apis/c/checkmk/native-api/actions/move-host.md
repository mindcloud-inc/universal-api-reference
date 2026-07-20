# Move Host with Checkmk

Moves an existing host to another Checkmk folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/objects/host_config/{host_name}/actions/move/invoke`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Move Host](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | path | `string` | yes | Checkmk host name to move. |
| `target_folder` | body | `string` | yes | Destination folder slug. |
