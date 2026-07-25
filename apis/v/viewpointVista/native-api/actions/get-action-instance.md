# Get Action Instance with Viewpoint Vista

Vista processes write operations asynchronously. This endpoint allows the integration to confirm whether a batch or time entry was successfully created.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/direct/actions/:action_key_value`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** Action Instance REST
- **Official documentation:** [Get Action Instance](https://direct-api.xchange.trimble.com/reference/get-directactionsaction_key_value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_key_value` | path | `string` | yes | Action Instance Identifier returned by an asynchronous Vista write operation. |
