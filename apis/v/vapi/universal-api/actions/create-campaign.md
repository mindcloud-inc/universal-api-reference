# Vapi: Create Campaign

Creates a new campaign in Vapi.

```
POST https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | This is the name of the campaign. This is just for your own reference. |
| `assistantId` | string | no | This is the assistant ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |
| `workflowId` | string | no | This is the workflow ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |
| `squadId` | string | no | This is the squad ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |
| `phoneNumberId` | string | no | This is the phone number ID that will be used for the campaign calls. Required if dialPlan is not provided. Note: phoneNumberId and dialPlan are mutually exclusive. |
| `dialPlan[]` | array<object> | no | This is a list of dial entries, each specifying a phone number and the customers to call using that number. Use this when you want different phone numbers to call different sets of customers. Note: phoneNumberId and dialPlan are mutually exclusive. |
| `schedulePlan` | object | no |  |
| `customers[]` | array<object> | no | These are the customers that will be called in the campaign. Required if dialPlan is not provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assistantId": "string",
      "calls": {},
      "callsCounterEnded": 1,
      "callsCounterEndedVoicemail": 1,
      "callsCounterInProgress": 1,
      "callsCounterQueued": 1,
      "callsCounterScheduled": 1,
      "createdAt": "string",
      "customers": [
        {}
      ],
      "dialPlan": [
        {}
      ],
      "endedReason": "string",
      "id": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "phoneNumberId": "string",
      "schedulePlan": {},
      "squadId": "string",
      "status": "string",
      "updatedAt": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assistantId` | string | This is the assistant ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |
| `calls` | object | This is a map of call IDs to campaign call details. |
| `callsCounterEnded` | number | This is the number of calls that have ended. |
| `callsCounterEndedVoicemail` | number | This is the number of calls whose ended reason is 'voicemail'. |
| `callsCounterInProgress` | number | This is the number of calls that have been in progress. |
| `callsCounterQueued` | number | This is the number of calls that have been queued. |
| `callsCounterScheduled` | number | This is the number of calls that have been scheduled. |
| `createdAt` | string | This is the ISO 8601 date-time string of when the campaign was created. |
| `customers` | array<object> | These are the customers that will be called in the campaign. Required if dialPlan is not provided. |
| `dialPlan` | array<object> | This is a list of dial entries, each specifying a phone number and the customers to call using that number. Use this when you want different phone numbers to call different sets of customers. Note: phoneNumberId and dialPlan are mutually exclusive. |
| `endedReason` | string | This is the explanation for how the campaign ended. |
| `id` | string | This is the unique identifier for the campaign. |
| `name` | string | This is the name of the campaign. This is just for your own reference. |
| `orgId` | string | This is the unique identifier for the org that this campaign belongs to. |
| `phoneNumberId` | string | This is the phone number ID that will be used for the campaign calls. Required if dialPlan is not provided. Note: phoneNumberId and dialPlan are mutually exclusive. |
| `schedulePlan` | object |  |
| `squadId` | string | This is the squad ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |
| `status` | string | This is the status of the campaign. |
| `updatedAt` | string | This is the ISO 8601 date-time string of when the campaign was last updated. |
| `workflowId` | string | This is the workflow ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |

## Native endpoint

Through the native Vapi API, this operation is `POST /campaign` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

