# Vapi: Create Call

Creates a new call in Vapi.

```
POST https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customers[]` | array<object> | no | This is used to issue batch calls to multiple customers. Only relevant for `outboundPhoneCall`. To call a single customer, use `customer` instead. |
| `customers[]` | array<object> | no | This is used to issue batch calls to multiple customers. Only relevant for `outboundPhoneCall`. To call a single customer, use `customer` instead. |
| `name` | string | no | This is the name of the call. This is just for your own reference. |
| `schedulePlan` | object | no |  |
| `transport` | object | no | This is the transport of the call. |
| `assistantId` | string | no | This is the assistant ID that will be used for the call. To use a transient assistant, use `assistant` instead. To start a call with: - Assistant, use `assistantId` or `assistant` - Squad, use `squadId` or `squad` - Workflow, use `workflowId` or `workflow` |
| `assistant` | object | no |  |
| `assistantOverrides` | object | no |  |
| `squadId` | string | no | This is the squad that will be used for the call. To use a transient squad, use `squad` instead. To start a call with: - Assistant, use `assistant` or `assistantId` - Squad, use `squad` or `squadId` - Workflow, use `workflow` or `workflowId` |
| `squad` | object | no |  |
| `squadOverrides` | object | no |  |
| `workflowId` | string | no | This is the workflow that will be used for the call. To use a transient workflow, use `workflow` instead. To start a call with: - Assistant, use `assistant` or `assistantId` - Squad, use `squad` or `squadId` - Workflow, use `workflow` or `workflowId` |
| `workflow` | object | no |  |
| `workflowOverrides` | object | no |  |
| `phoneNumberId` | string | no | This is the phone number that will be used for the call. To use a transient number, use `phoneNumber` instead. Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `phoneNumber` | object | no |  |
| `customerId` | string | no | This is the customer that will be called. To call a transient customer , use `customer` instead. Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `customer` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {},
      "artifact": {},
      "artifactPlan": {},
      "assistant": {},
      "assistantId": "string",
      "assistantOverrides": {},
      "campaignId": "string",
      "compliance": {},
      "cost": 1,
      "costBreakdown": {},
      "costs": [
        {}
      ],
      "createdAt": "string",
      "customer": {},
      "customerId": "string",
      "destination": {},
      "endedAt": "string",
      "endedMessage": "string",
      "endedReason": "string",
      "id": "string",
      "messages": [
        {}
      ],
      "monitor": {},
      "name": "Ava Chen",
      "orgId": "string",
      "phoneCallProvider": "string",
      "phoneCallProviderId": "string",
      "phoneCallTransport": "string",
      "phoneNumber": {},
      "phoneNumberId": "string",
      "schedulePlan": {},
      "squad": {},
      "squadId": "string",
      "squadOverrides": {},
      "startedAt": "string",
      "status": "string",
      "transport": {},
      "type": "string",
      "updatedAt": "string",
      "workflow": {},
      "workflowId": "string",
      "workflowOverrides": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis` | object |  |
| `artifact` | object |  |
| `artifactPlan` | object |  |
| `assistant` | object |  |
| `assistantId` | string | This is the assistant ID that will be used for the call. To use a transient assistant, use `assistant` instead.  To start a call with: - Assistant, use `assistantId` or `assistant` - Squad, use `squadId` or `squad` - Workflow, use `workflowId` or `workflow` |
| `assistantOverrides` | object |  |
| `campaignId` | string | This is the campaign ID that the call belongs to. |
| `compliance` | object |  |
| `cost` | number | This is the cost of the call in USD. |
| `costBreakdown` | object |  |
| `costs` | array<object> | These are the costs of individual components of the call in USD. |
| `createdAt` | string | This is the ISO 8601 date-time string of when the call was created. |
| `customer` | object |  |
| `customerId` | string | This is the customer that will be called. To call a transient customer , use `customer` instead.  Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `destination` | object |  |
| `endedAt` | string | This is the ISO 8601 date-time string of when the call was ended. |
| `endedMessage` | string | This is the message that adds more context to the ended reason. It can be used to provide potential error messages or warnings. |
| `endedReason` | string | This is the explanation for how the call ended. |
| `id` | string | This is the unique identifier for the call. |
| `messages` | array<object> |  |
| `monitor` | object |  |
| `name` | string | This is the name of the call. This is just for your own reference. |
| `orgId` | string | This is the unique identifier for the org that this call belongs to. |
| `phoneCallProvider` | string | This is the provider of the call.  Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `phoneCallProviderId` | string | The ID of the call as provided by the phone number service. callSid in Twilio. conversationUuid in Vonage. callControlId in Telnyx.  Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `phoneCallTransport` | string | This is the transport of the phone call.  Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `phoneNumber` | object |  |
| `phoneNumberId` | string | This is the phone number that will be used for the call. To use a transient number, use `phoneNumber` instead.  Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `schedulePlan` | object |  |
| `squad` | object |  |
| `squadId` | string | This is the squad that will be used for the call. To use a transient squad, use `squad` instead.  To start a call with: - Assistant, use `assistant` or `assistantId` - Squad, use `squad` or `squadId` - Workflow, use `workflow` or `workflowId` |
| `squadOverrides` | object |  |
| `startedAt` | string | This is the ISO 8601 date-time string of when the call was started. |
| `status` | string | This is the status of the call. |
| `transport` | object | This is the transport of the call. |
| `type` | string | This is the type of call. |
| `updatedAt` | string | This is the ISO 8601 date-time string of when the call was last updated. |
| `workflow` | object |  |
| `workflowId` | string | This is the workflow that will be used for the call. To use a transient workflow, use `workflow` instead.  To start a call with: - Assistant, use `assistant` or `assistantId` - Squad, use `squad` or `squadId` - Workflow, use `workflow` or `workflowId` |
| `workflowOverrides` | object |  |

## Native endpoint

Through the native Vapi API, this operation is `POST /call` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-call.md) for the provider-specific parameters and requirements.

