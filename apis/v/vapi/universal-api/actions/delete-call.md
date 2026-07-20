# Vapi: Delete Call

Deletes an existing call from Vapi.

```
DELETE https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-call?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-call?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `ids[]` | array<string> | no | These are the Call IDs to be bulk deleted. If provided, the call ID if any in the request query will be ignored When requesting a bulk delete, updates when a call is deleted will be sent as a webhook to the server URL configured in the Org settings. It may take up to a few hours to complete the bulk delete, and will be asynchronous. |
| `ids[]` | array<string> | no | These are the Call IDs to be bulk deleted. If provided, the call ID if any in the request query will be ignored When requesting a bulk delete, updates when a call is deleted will be sent as a webhook to the server URL configured in the Org settings. It may take up to a few hours to complete the bulk delete, and will be asynchronous. |

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

Through the native Vapi API, this operation is `DELETE /call/:id` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-call.md) for the provider-specific parameters and requirements.

