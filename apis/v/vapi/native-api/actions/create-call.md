# Create Call with Vapi

Creates a new call in Vapi.

## Endpoint

- **Method:** `POST`
- **Path:** `/call`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Create Call](https://docs.vapi.ai/api-reference/calls/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customers[]` | body | `array<object>` | no | This is used to issue batch calls to multiple customers.  Only relevant for `outboundPhoneCall`. To call a single customer, use `customer` instead. |
| `customers[]` | body | `array<object>` | no | This is used to issue batch calls to multiple customers.  Only relevant for `outboundPhoneCall`. To call a single customer, use `customer` instead. |
| `name` | body | `string` | no | This is the name of the call. This is just for your own reference. |
| `schedulePlan` | body | `object` | no | — |
| `transport` | body | `object` | no | This is the transport of the call. |
| `assistantId` | body | `string` | no | This is the assistant ID that will be used for the call. To use a transient assistant, use `assistant` instead.  To start a call with: - Assistant, use `assistantId` or `assistant` - Squad, use `squadId` or `squad` - Workflow, use `workflowId` or `workflow` |
| `assistant` | body | `object` | no | — |
| `assistantOverrides` | body | `object` | no | — |
| `squadId` | body | `string` | no | This is the squad that will be used for the call. To use a transient squad, use `squad` instead.  To start a call with: - Assistant, use `assistant` or `assistantId` - Squad, use `squad` or `squadId` - Workflow, use `workflow` or `workflowId` |
| `squad` | body | `object` | no | — |
| `squadOverrides` | body | `object` | no | — |
| `workflowId` | body | `string` | no | This is the workflow that will be used for the call. To use a transient workflow, use `workflow` instead.  To start a call with: - Assistant, use `assistant` or `assistantId` - Squad, use `squad` or `squadId` - Workflow, use `workflow` or `workflowId` |
| `workflow` | body | `object` | no | — |
| `workflowOverrides` | body | `object` | no | — |
| `phoneNumberId` | body | `string` | no | This is the phone number that will be used for the call. To use a transient number, use `phoneNumber` instead.  Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `phoneNumber` | body | `object` | no | — |
| `customerId` | body | `string` | no | This is the customer that will be called. To call a transient customer , use `customer` instead.  Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `customer` | body | `object` | no | — |
