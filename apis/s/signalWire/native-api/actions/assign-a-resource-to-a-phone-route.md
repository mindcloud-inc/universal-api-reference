# Assign a Resource to a Phone Route with SignalWire

Assigns a resource to a phone route in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/{id}/phone_routes`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Assign a Resource to a Phone Route](https://signalwire.com/docs/apis/rest/phone-numbers/assign-resource-phone-route)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Resource. |
| `phone_route_id` | body | `string` | yes | The id of the phone route. |
| `handler` | body | `string` | yes | Indicates if the resource should be assigned to a `calling` or `messaging` handler. |
