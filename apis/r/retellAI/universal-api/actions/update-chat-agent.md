# Retell AI: Update Chat Agent

Updates a chat agent in Retell AI.

```
PUT https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-chat-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-chat-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "piiConfig.categories[]": [
    "string"
  ],
  "responseEngine.type": "string",
  "responseEngine.llmId": "string",
  "postChatAnalysisData[].type": "string",
  "postChatAnalysisData[].name": "Ava Chen",
  "postChatAnalysisData[].description": "string",
  "piiConfig.mode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-chat-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "piiConfig.categories[]": ["string"],
    "responseEngine.type": "string",
    "responseEngine.llmId": "string",
    "postChatAnalysisData[].type": "string",
    "postChatAnalysisData[].name": "Ava Chen",
    "postChatAnalysisData[].description": "string",
    "piiConfig.mode": "string",
    "piiConfig.categories[]": ["string"],
    "piiConfig.categories[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |
| `guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `guardrailConfig.outputTopics[]` | array<string> | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `postChatAnalysisData[]` | array<object> | no | Post chat analysis data to extract from the chat. This data will augment the pre-defined variables extracted in the chat analysis. This will be available after the chat ends. |
| `postChatAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to chat_started, chat_ended, chat_analyzed. |
| `version` | number | no |  |
| `responseEngine` | object | no |  |
| `responseEngine.type` | string | yes | type of the Response Engine. Allowed values: retell-llm. |
| `responseEngine.llmId` | string | yes | id of the Retell LLM Response Engine. |
| `responseEngine.version` | number | no | Version of the Retell LLM Response Engine. |
| `agentName` | string | no | The name of the chat agent. Only used for your own reference. |
| `autoCloseMessage` | string | no | Message to display when the chat is automatically closed. |
| `endChatAfterSilenceMs` | number | no | If users stay silent for a period after agent speech, end the chat. The minimum value allowed is 120,000 ms (2 minutes). The maximum value allowed is 259,200,000 ms (72 hours). By default, this is set to 3,600,000 (1 hour). |
| `language` | string | no | Specifies what language (and dialect) the chat will operate in. For instance, selecting `en-GB` optimizes for British English. If unset, will use default value `en-US`. Select `multi` for multilingual support, currently this supports Spanish and English. |
| `webhookUrl` | string | no | The webhook for agent to listen to chat events. See what events it would get at [webhook doc](/features/webhook). If set, will binds webhook events for this agent to the specified url, and will ignore the account level webhook for this agent. Set to `null` to remove webhook url from this agent. |
| `webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to chat_started, chat_ended, chat_analyzed. |
| `webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to chat_started, chat_ended, chat_analyzed. |
| `webhookTimeoutMs` | number | no | The timeout for the webhook in milliseconds. If not set, default value of 10000 will apply. |
| `dataStorageSetting` | string | no | Controls what data is stored for this agent. "everything" stores all data including transcripts and recordings. "everything_except_pii" stores data but excludes PII when possible based on PII configuration. "basic_attributes_only" stores only basic metadata. If not set, defaults to "everything". Allowed values: everything, everything_except_pii, basic_attributes_only. |
| `dataStorageRetentionDays` | number | no | Number of days to retain call/chat data before automatic deletion. Must be between 1 and 730 days. If not set, data is retained forever (no automatic deletion). |
| `optInSignedUrl` | boolean | no | Whether this agent opts in to signed url for public log. If not set, default value of false will apply. |
| `signedUrlExpirationMs` | number | no | The expiration time for the signed url in milliseconds. Only applicable when opt_in_signed_url is true. If not set, default value of 86400000 (24 hours) will apply. |
| `postChatAnalysisData[]` | array<object> | no | Post chat analysis data to extract from the chat. This data will augment the pre-defined variables extracted in the chat analysis. This will be available after the chat ends. |
| `postChatAnalysisData[]` | array<object> | no | Post chat analysis data to extract from the chat. This data will augment the pre-defined variables extracted in the chat analysis. This will be available after the chat ends. |
| `postChatAnalysisData[].type` | string | yes | Type of the variable to extract. Allowed values: string. |
| `postChatAnalysisData[].name` | string | yes | Name of the variable. |
| `postChatAnalysisData[].description` | string | yes | Description of the variable. |
| `postChatAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `postChatAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `postChatAnalysisData[].required` | boolean | no | Whether this data is required. If true and the data is not extracted, the call will be marked as unsuccessful. |
| `postChatAnalysisModel` | string | no | Available LLM models for agents. |
| `analysisSuccessfulPrompt` | string | no | The prompt to use for post call analysis to evaluate whether the call is successful. Set to null to use the default prompt. |
| `analysisSummaryPrompt` | string | no | The prompt to use for post call analysis to summarize the call. Set to null to use the default prompt. |
| `analysisUserSentimentPrompt` | string | no | Prompt to guide how the post chat analysis should evaluate user sentiment. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `piiConfig` | object | no |  |
| `piiConfig.mode` | string | yes | The processing mode for PII scrubbing. Currently only post-call is supported. Allowed values: post_call. |
| `piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `guardrailConfig` | object | no |  |
| `guardrailConfig.outputTopics[]` | array<string> | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `guardrailConfig.outputTopics[]` | array<string> | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `isPublic` | boolean | no | Whether the agent is public. When set to true, the agent is available for public agent preview link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "agentName": "Ava Chen",
      "analysisSuccessfulPrompt": "string",
      "analysisSummaryPrompt": "string",
      "analysisUserSentimentPrompt": "string",
      "autoCloseMessage": "string",
      "dataStorageRetentionDays": 1,
      "dataStorageSetting": "string",
      "endChatAfterSilenceMs": 1,
      "guardrailConfig": {
        "inputTopics": [
          "string"
        ],
        "outputTopics": [
          "string"
        ]
      },
      "isPublic": true,
      "isPublished": true,
      "language": "string",
      "lastModificationTimestamp": 1,
      "optInSignedUrl": true,
      "piiConfig": {
        "categories": [
          "string"
        ],
        "mode": "string"
      },
      "postChatAnalysisData": [
        {
          "description": "string",
          "examples": [
            "string"
          ],
          "name": "Ava Chen",
          "required": true,
          "type": "string"
        }
      ],
      "postChatAnalysisModel": "string",
      "responseEngine": {
        "llmId": "string",
        "type": "string",
        "version": 1
      },
      "signedUrlExpirationMs": 1,
      "version": 1,
      "webhookEvents": [
        "string"
      ],
      "webhookTimeoutMs": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Unique id of chat agent. |
| `agentName` | string | The name of the chat agent. Only used for your own reference. |
| `analysisSuccessfulPrompt` | string | The prompt to use for post call analysis to evaluate whether the call is successful. Set to null to use the default prompt. |
| `analysisSummaryPrompt` | string | The prompt to use for post call analysis to summarize the call. Set to null to use the default prompt. |
| `analysisUserSentimentPrompt` | string | Prompt to guide how the post chat analysis should evaluate user sentiment. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `autoCloseMessage` | string | Message to display when the chat is automatically closed. |
| `dataStorageRetentionDays` | number | Number of days to retain call/chat data before automatic deletion. Must be between 1 and 730 days. If not set, data is retained forever (no automatic deletion). |
| `dataStorageSetting` | string | Controls what data is stored for this agent. "everything" stores all data including transcripts and recordings. "everything_except_pii" stores data but excludes PII when possible based on PII configuration. "basic_attributes_only" stores only basic metadata. If not set, defaults to "everything". Allowed values: everything, everything_except_pii, basic_attributes_only. |
| `endChatAfterSilenceMs` | number | If users stay silent for a period after agent speech, end the chat. The minimum value allowed is 120,000 ms (2 minutes). The maximum value allowed is 259,200,000 ms (72 hours). By default, this is set to 3,600,000 (1 hour). |
| `guardrailConfig` | object |  |
| `guardrailConfig.inputTopics` | array<string> | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `guardrailConfig.outputTopics` | array<string> | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `isPublic` | boolean | Whether the agent is public. When set to true, the agent is available for public agent preview link. |
| `isPublished` | boolean | Whether the chat agent is published. |
| `language` | string | Specifies what language (and dialect) the chat will operate in. For instance, selecting `en-GB` optimizes for British English. If unset, will use default value `en-US`. Select `multi` for multilingual support, currently this supports Spanish and English. |
| `lastModificationTimestamp` | number | Last modification timestamp (milliseconds since epoch). Either the time of last update or creation if no updates available. |
| `optInSignedUrl` | boolean | Whether this agent opts in to signed url for public log. If not set, default value of false will apply. |
| `piiConfig` | object |  |
| `piiConfig.categories` | array<string> | List of PII categories to scrub from transcripts and recordings. |
| `piiConfig.mode` | string | The processing mode for PII scrubbing. Currently only post-call is supported. Allowed values: post_call. |
| `postChatAnalysisData` | array<object> | Post chat analysis data to extract from the chat. This data will augment the pre-defined variables extracted in the chat analysis. This will be available after the chat ends. |
| `postChatAnalysisData[].description` | string | Description of the variable. |
| `postChatAnalysisData[].examples` | array<string> | Examples of the variable value to teach model the style and syntax. |
| `postChatAnalysisData[].name` | string | Name of the variable. |
| `postChatAnalysisData[].required` | boolean | Whether this data is required. If true and the data is not extracted, the call will be marked as unsuccessful. |
| `postChatAnalysisData[].type` | string | Type of the variable to extract. Allowed values: string. |
| `postChatAnalysisModel` | string | Available LLM models for agents. |
| `responseEngine` | object |  |
| `responseEngine.llmId` | string | id of the Retell LLM Response Engine. |
| `responseEngine.type` | string | type of the Response Engine. Allowed values: retell-llm. |
| `responseEngine.version` | number | Version of the Retell LLM Response Engine. |
| `signedUrlExpirationMs` | number | The expiration time for the signed url in milliseconds. Only applicable when opt_in_signed_url is true. If not set, default value of 86400000 (24 hours) will apply. |
| `version` | number | The version of the chat agent. |
| `webhookEvents` | array<string> | Which webhook events this agent should receive. If not set, defaults to chat_started, chat_ended, chat_analyzed. |
| `webhookTimeoutMs` | number | The timeout for the webhook in milliseconds. If not set, default value of 10000 will apply. |
| `webhookUrl` | string | The webhook for agent to listen to chat events. See what events it would get at [webhook doc](/features/webhook). If set, will binds webhook events for this agent to the specified url, and will ignore the account level webhook for this agent. Set to `null` to remove webhook url from this agent. |

## Native endpoint

Through the native Retell AI API, this operation is `PATCH /update-chat-agent/{agent_id}` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat-agent.md) for the provider-specific parameters and requirements.

