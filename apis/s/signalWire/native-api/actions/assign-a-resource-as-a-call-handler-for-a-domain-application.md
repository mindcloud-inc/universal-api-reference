# Assign a resource as a call handler for a Domain Application. with SignalWire

Assigns a resource as a call handler for a domain application in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/{id}/domain_applications`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Assign a resource as a call handler for a Domain Application.](https://signalwire.com/docs/apis/rest/domain-applications/assign-resource-domain-application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Resource. |
| `domain_application_id` | body | `string` | yes | The id of the domain application you wish to assign a resource to. |
