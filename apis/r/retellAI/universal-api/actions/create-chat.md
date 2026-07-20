# Retell AI: Create Chat

Creates a chat in Retell AI.

```
POST https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The chat agent to use for the call. |
| `agentVersion` | number | no | The version of the chat agent to use for the chat. If not provided, will default to latest version. |
| `metadata` | object | no | An arbitrary object for storage purpose only. You can put anything here like your internal customer id associated with the chat. Not used for processing. You can later get this field from the chat object. |
| `retellLlmDynamicVariables` | object | no | Add optional dynamic variables in key value pairs of string that injects into your Response Engine prompt and tool description. Only applicable for Response Engine. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "chatAnalysis": {
        "chatSuccessful": true,
        "chatSummary": "string",
        "customAnalysisData": {},
        "userSentiment": "string"
      },
      "chatCost": {
        "combinedCost": 1,
        "productCosts": [
          {
            "cost": 1,
            "isTransferLegCost": true,
            "product": "string",
            "unitPrice": 1
          }
        ]
      },
      "chatId": "string",
      "chatStatus": "string",
      "chatType": "string",
      "collectedDynamicVariables": {},
      "customAttributes": {},
      "endTimestamp": 1,
      "messageWithToolCalls": [
        {
          "content": "string",
          "createdTimestamp": 1,
          "messageId": "string",
          "role": "string"
        }
      ],
      "metadata": {},
      "retellLlmDynamicVariables": {},
      "startTimestamp": 1,
      "transcript": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Corresponding chat agent id of this chat. |
| `chatAnalysis` | object |  |
| `chatAnalysis.chatSuccessful` | boolean | Whether the agent seems to have a successful chat with the user, where the agent finishes the task, and the call was complete without being cutoff. |
| `chatAnalysis.chatSummary` | string | A high level summary of the chat. |
| `chatAnalysis.customAnalysisData` | object | Custom analysis data that was extracted based on the schema defined in chat agent post chat analysis data. Can be empty if nothing is specified. |
| `chatAnalysis.userSentiment` | string | Sentiment of the user in the chat. Allowed values: Negative, Positive, Neutral, Unknown. |
| `chatCost` | object |  |
| `chatCost.combinedCost` | number | Combined cost of all individual costs in cents |
| `chatCost.productCosts` | array<object> | List of products with their unit prices and costs in cents |
| `chatCost.productCosts[].cost` | number | Cost for the product in cents for the duration of the call. |
| `chatCost.productCosts[].isTransferLegCost` | boolean | True if this cost item is for a transfer segment. |
| `chatCost.productCosts[].product` | string | Product name that has a cost associated with it. |
| `chatCost.productCosts[].unitPrice` | number | Unit price of the product in cents per second. |
| `chatId` | string | Unique id of the chat. |
| `chatStatus` | string | Status of chat.  - `ongoing`: Chat session is ongoing, chat agent can receive new message and generate response. - `ended`: Chat session has ended, and no longer can generate new response. - `error`: Chat encountered error. Allowed values: ongoing, ended, error. |
| `chatType` | string | Type of the chat Allowed values: api_chat, sms_chat. |
| `collectedDynamicVariables` | object | Dynamic variables collected from the chat. Only available after the chat ends. |
| `customAttributes` | object | Custom attributes for the chat |
| `endTimestamp` | number | End timestamp (milliseconds since epoch) of the chat. Available after chat ends. |
| `messageWithToolCalls` | array<object> | Transcript of the chat weaved with tool call invocation and results. |
| `messageWithToolCalls[].content` | string | Content of the message |
| `messageWithToolCalls[].createdTimestamp` | number | Create timestamp of the message |
| `messageWithToolCalls[].messageId` | string | Unique id of the message |
| `messageWithToolCalls[].role` | string | Documents whether this message is sent by agent or user. Allowed values: agent, user. |
| `metadata` | object | An arbitrary object for storage purpose only. You can put anything here like your internal customer id associated with the chat. Not used for processing. You can later get this field from the chat object. |
| `retellLlmDynamicVariables` | object | Add optional dynamic variables in key value pairs of string that injects into your Response Engine prompt and tool description. Only applicable for Response Engine. |
| `startTimestamp` | number | Begin timestamp (milliseconds since epoch) of the chat. Available after chat starts. |
| `transcript` | string | Transcription of the chat. |
| `version` | number | The version of the agent |

## Native endpoint

Through the native Retell AI API, this operation is `POST /create-chat` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat.md) for the provider-specific parameters and requirements.

