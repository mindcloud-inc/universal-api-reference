# Chatvolt AI: Move Conversation to CRM Step

Moves a conversation to a CRM step in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-move-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-move-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-move-step', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | ID of the conversation to move. |
| `scenarioId` | string | no | ID of the CRM scenario. Required if `destStepId` is not provided or to specify context for `destStepIndex`. |
| `destStepId` | string | no | ID of the destination CRM step. If provided, `scenarioId` (if also provided) must match the step's scenario. |
| `destStepIndex` | number | no | Index of the destination step within the scenario (used with `scenarioId` if `destStepId` is not provided). |
| `shouldSendInitialMessage` | boolean | no | Whether to send the initial message of the destination step. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockedBy24hRule": true,
      "message": "string",
      "messageError": "string",
      "messageSent": true,
      "newStepId": "string",
      "sentMessageId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockedBy24hRule` | boolean | Indicates if sending a message was blocked by the 24-hour rule (e.g., for WhatsApp). |
| `message` | string | Message. |
| `messageError` | string | Error message if sending the initial message failed. |
| `messageSent` | boolean | Indicates if the initial message of the new step was sent. |
| `newStepId` | string | The ID of the new step the conversation was moved to. |
| `sentMessageId` | string | The ID of the message that was sent (if any). |
| `success` | boolean | Success. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /crm/step/move` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-step-move-step.md) for the provider-specific parameters and requirements.

