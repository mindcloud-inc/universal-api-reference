# Show Host Service with Checkmk

Retrieves monitored service details for a Checkmk host.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/host/{host_name}/actions/show_service/invoke`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Show Host Service](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | path | `string` | yes | Checkmk host name. |
| `service_description` | query | `string` | yes | Exact Checkmk service description. |
