# Deploy Call Flow Version with SignalWire

Deploys a call flow version in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/call_flow/{id}/versions`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Deploy Call Flow Version](https://signalwire.com/docs/apis/rest/call-flows/deploy-call-flow-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Call Flow. |
| `document_version` | body | `number` | yes | The current revision of the call flow. |
