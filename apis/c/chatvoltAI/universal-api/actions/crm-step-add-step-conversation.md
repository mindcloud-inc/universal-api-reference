# Chatvolt AI: Add Conversation to CRM Step

Adds a conversation to a CRM step in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-add-step-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-add-step-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-add-step-conversation', {
  method: 'POST',
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
| `conversationId` | string | yes | ID of the conversation to add to the step. |
| `scenarioId` | string | no | ID of the CRM scenario. Required if `stepId` is not provided or if `stepIndex` is used. |
| `stepId` | string | no | ID of the specific CRM step. If provided, `scenarioId` and `stepIndex` are ignored for step identification. |
| `stepIndex` | number | no | Index of the step within the scenario (used with `scenarioId` if `stepId` is not provided). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockedBy24hRule": true,
      "initialMessage": "string",
      "message": "string",
      "messageSent": true,
      "newStepId": "string",
      "sendMessageError": "string",
      "sentMessageId": "string",
      "stepAgentId": "string",
      "success": true,
      "zapiAgentId": "string",
      "zapiMessage": "string",
      "zapiPhoneNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockedBy24hRule` | boolean | BlockedBy24hRule. |
| `initialMessage` | string | InitialMessage. |
| `message` | string | Message. |
| `messageSent` | boolean | MessageSent. |
| `newStepId` | string | NewStepId. |
| `sendMessageError` | string | SendMessageError. |
| `sentMessageId` | string | SentMessageId. |
| `stepAgentId` | string | StepAgentId. |
| `success` | boolean | Success. |
| `zapiAgentId` | string | ZapiAgentId. |
| `zapiMessage` | string | ZapiMessage. |
| `zapiPhoneNumber` | string | ZapiPhoneNumber. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /crm/step/conversation` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-step-add-step-conversation.md) for the provider-specific parameters and requirements.

