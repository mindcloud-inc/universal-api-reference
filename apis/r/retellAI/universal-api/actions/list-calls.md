# Retell AI: List Calls

Retrieves calls from Retell AI.

```
GET https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-calls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-calls?${params}`, {
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
| `filterCriteria` | object | no | Filter criteria for the calls to retrieve. |
| `filterCriteria.agentId[]` | array<string> | no | Only retrieve calls that are made with specific agent(s). |
| `filterCriteria.batchCallId[]` | array<string> | no | Only retrieve calls with specific batch call id(s). |
| `filterCriteria.callStatus[]` | array<string> | no | Only retrieve calls with specific call status(es). |
| `filterCriteria.callSuccessful[]` | array<boolean> | no | Only retrieve calls with specific call successful(s). |
| `filterCriteria.callType[]` | array<string> | no | Only retrieve calls with specific call type(s). |
| `filterCriteria.direction[]` | array<string> | no | Only retrieve calls with specific direction(s). |
| `filterCriteria.disconnectionReason[]` | array<string> | no | Only retrieve calls with specific disconnection reason(s). |
| `filterCriteria.fromNumber[]` | array<string> | no | Only retrieve calls with specific from number(s). |
| `filterCriteria.inVoicemail[]` | array<boolean> | no | Only retrieve calls that are in voicemail or not in voicemail. |
| `filterCriteria.toNumber[]` | array<string> | no | Only retrieve calls with specific to number(s). |
| `filterCriteria.userSentiment[]` | array<string> | no | Only retrieve calls with specific user sentiment(s). |
| `filterCriteria.version[]` | array<number> | no | The version of the agent to use for the call. |
| `filterCriteria.agentId[]` | array<string> | no | Only retrieve calls that are made with specific agent(s). |
| `filterCriteria.agentId[]` | array<string> | no | Only retrieve calls that are made with specific agent(s). |
| `filterCriteria.version[]` | array<number> | no | The version of the agent to use for the call. |
| `filterCriteria.version[]` | array<number> | no | The version of the agent to use for the call. |
| `filterCriteria.callStatus[]` | array<string> | no | Only retrieve calls with specific call status(es). |
| `filterCriteria.callStatus[]` | array<string> | no | Only retrieve calls with specific call status(es). |
| `filterCriteria.inVoicemail[]` | array<boolean> | no | Only retrieve calls that are in voicemail or not in voicemail. |
| `filterCriteria.inVoicemail[]` | array<boolean> | no | Only retrieve calls that are in voicemail or not in voicemail. |
| `filterCriteria.disconnectionReason[]` | array<string> | no | Only retrieve calls with specific disconnection reason(s). |
| `filterCriteria.disconnectionReason[]` | array<string> | no | Only retrieve calls with specific disconnection reason(s). |
| `filterCriteria.fromNumber[]` | array<string> | no | Only retrieve calls with specific from number(s). |
| `filterCriteria.fromNumber[]` | array<string> | no | Only retrieve calls with specific from number(s). |
| `filterCriteria.toNumber[]` | array<string> | no | Only retrieve calls with specific to number(s). |
| `filterCriteria.toNumber[]` | array<string> | no | Only retrieve calls with specific to number(s). |
| `filterCriteria.batchCallId[]` | array<string> | no | Only retrieve calls with specific batch call id(s). |
| `filterCriteria.batchCallId[]` | array<string> | no | Only retrieve calls with specific batch call id(s). |
| `filterCriteria.callType[]` | array<string> | no | Only retrieve calls with specific call type(s). |
| `filterCriteria.callType[]` | array<string> | no | Only retrieve calls with specific call type(s). |
| `filterCriteria.direction[]` | array<string> | no | Only retrieve calls with specific direction(s). |
| `filterCriteria.direction[]` | array<string> | no | Only retrieve calls with specific direction(s). |
| `filterCriteria.userSentiment[]` | array<string> | no | Only retrieve calls with specific user sentiment(s). |
| `filterCriteria.userSentiment[]` | array<string> | no | Only retrieve calls with specific user sentiment(s). |
| `filterCriteria.callSuccessful[]` | array<boolean> | no | Only retrieve calls with specific call successful(s). |
| `filterCriteria.callSuccessful[]` | array<boolean> | no | Only retrieve calls with specific call successful(s). |
| `filterCriteria.startTimestamp` | object | no | Only retrieve calls with specific range of start timestamp(s). |
| `filterCriteria.startTimestamp.upperThreshold` | number | no |  |
| `filterCriteria.startTimestamp.lowerThreshold` | number | no |  |
| `filterCriteria.endTimestamp` | object | no | Only retrieve calls with specific range of end timestamp(s). |
| `filterCriteria.endTimestamp.upperThreshold` | number | no |  |
| `filterCriteria.endTimestamp.lowerThreshold` | number | no |  |
| `filterCriteria.durationMs` | object | no | Only retrieve calls with specific range of duration(s). |
| `filterCriteria.durationMs.upperThreshold` | number | no |  |
| `filterCriteria.durationMs.lowerThreshold` | number | no |  |
| `filterCriteria.e2eLatencyP50` | object | no |  |
| `filterCriteria.e2eLatencyP50.upperThreshold` | number | no |  |
| `filterCriteria.e2eLatencyP50.lowerThreshold` | number | no |  |
| `filterCriteria.metadata` | object | no | Filter by metadata fields using dot notation (e.g., `metadata.customer_id`). Values are matched exactly as strings. |
| `filterCriteria.dynamicVariables` | object | no | Filter by dynamic variables using dot notation (e.g., `dynamic_variables.name`). Values are matched exactly as strings. |
| `sortOrder` | string | no | The calls will be sorted by `start_timestamp`, whether to return the calls in ascending or descending order. Allowed values: ascending, descending. |
| `limit` | number | no | Limit the number of calls returned. Default 50, Max 1000. To retrieve more than 1000, use pagination_key to continue fetching the next page. |
| `paginationKey` | string | no | The pagination key to continue fetching the next page of calls. Pagination key is represented by a call id here, and it's exclusive (not included in the fetched calls). The last call id from the list calls is usually used as pagination key here. If not set, will start from the beginning. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "agentId": "string",
      "agentName": "Ava Chen",
      "agentVersion": 1,
      "callAnalysis": {
        "callSuccessful": true,
        "callSummary": "string",
        "customAnalysisData": {},
        "inVoicemail": true,
        "userSentiment": "string"
      },
      "callCost": {
        "combinedCost": 1,
        "productCosts": [
          {
            "cost": 1,
            "isTransferLegCost": true,
            "product": "string",
            "unitPrice": 1
          }
        ],
        "totalDurationSeconds": 1,
        "totalDurationUnitPrice": 1
      },
      "callId": "string",
      "callStatus": "string",
      "callType": "string",
      "collectedDynamicVariables": {},
      "customSipHeaders": {},
      "dataStorageSetting": "string",
      "disconnectionReason": "string",
      "durationMs": 1,
      "endTimestamp": 1,
      "knowledgeBaseRetrievedContentsUrl": "https://example.com",
      "latency": {
        "asr": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "e2e": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "knowledgeBase": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "llm": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "llmWebsocketNetworkRtt": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "s2s": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "tts": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        }
      },
      "llmTokenUsage": {
        "average": 1,
        "numRequests": 1,
        "values": [
          1
        ]
      },
      "metadata": {},
      "optInSignedUrl": true,
      "publicLogUrl": "https://example.com",
      "recordingMultiChannelUrl": "https://example.com",
      "recordingUrl": "https://example.com",
      "retellLlmDynamicVariables": {},
      "scrubbedRecordingMultiChannelUrl": "https://example.com",
      "scrubbedRecordingUrl": "https://example.com",
      "scrubbedTranscriptWithToolCalls": [
        {
          "content": "string",
          "role": "string",
          "words": [
            {
              "end": 1,
              "start": 1,
              "word": "string"
            }
          ]
        }
      ],
      "startTimestamp": 1,
      "transcript": "string",
      "transcriptObject": [
        {
          "content": "string",
          "role": "string",
          "words": [
            {
              "end": 1,
              "start": 1,
              "word": "string"
            }
          ]
        }
      ],
      "transcriptWithToolCalls": [
        {
          "content": "string",
          "role": "string",
          "words": [
            {
              "end": 1,
              "start": 1,
              "word": "string"
            }
          ]
        }
      ],
      "transferDestination": "string",
      "transferEndTimestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Access token to enter the web call room. This needs to be passed to your frontend to join the call. |
| `agentId` | string | Corresponding agent id of this call. |
| `agentName` | string | Name of the agent. |
| `agentVersion` | number | The version of the agent. |
| `callAnalysis` | object |  |
| `callAnalysis.callSuccessful` | boolean | Whether the agent seems to have a successful call with the user, where the agent finishes the task, and the call was complete without being cutoff. |
| `callAnalysis.callSummary` | string | A high level summary of the call. |
| `callAnalysis.customAnalysisData` | object | Custom analysis data that was extracted based on the schema defined in agent post call analysis data. Can be empty if nothing is specified. |
| `callAnalysis.inVoicemail` | boolean | Whether the call is entered voicemail. |
| `callAnalysis.userSentiment` | string | Sentiment of the user in the call. Allowed values: Negative, Positive, Neutral, Unknown. |
| `callCost` | object | Cost of the call, including all the products and their costs and discount. |
| `callCost.combinedCost` | number | Combined cost of all individual costs in cents |
| `callCost.productCosts` | array<object> | List of products with their unit prices and costs in cents |
| `callCost.productCosts[].cost` | number | Cost for the product in cents for the duration of the call. |
| `callCost.productCosts[].isTransferLegCost` | boolean | True if this cost item is for a transfer segment. |
| `callCost.productCosts[].product` | string | Product name that has a cost associated with it. |
| `callCost.productCosts[].unitPrice` | number | Unit price of the product in cents per second. |
| `callCost.totalDurationSeconds` | number | Total duration of the call in seconds |
| `callCost.totalDurationUnitPrice` | number | Total unit duration price of all products in cents per second |
| `callId` | string | Unique id of the call. Used to identify the call in the LLM websocket and used to authenticate in the audio websocket. |
| `callStatus` | string | Status of call.  - `registered`: Call id issued, starting to make a call using this id. - `ongoing`: Call connected and ongoing. - `ended`: The underlying websocket has ended for the call. Either user or agent hung up, or call transferred. - `error`: Call encountered error. Allowed values: registered, not_connected, ongoing, ended, error. |
| `callType` | string | Type of the call. Used to distinguish between web call and phone call. Allowed values: web_call. |
| `collectedDynamicVariables` | object | Dynamic variables collected from the call. Only available after the call ends. |
| `customSipHeaders` | object | Custom SIP headers to be added to the call. |
| `dataStorageSetting` | string | Data storage setting for this call's agent. "everything" stores all data, "everything_except_pii" excludes PII when possible, "basic_attributes_only" stores only metadata. Allowed values: everything, everything_except_pii, basic_attributes_only. |
| `disconnectionReason` | string |  |
| `durationMs` | number | Duration of the call in milliseconds. Available after call ends. |
| `endTimestamp` | number | End timestamp (milliseconds since epoch) of the call. Available after call ends. |
| `knowledgeBaseRetrievedContentsUrl` | string | URL to the knowledge base retrieved contents of the call. Available after call ends if the call utilizes knowledge base feature. It consists of the respond id and the retrieved contents related to that response. It's already rendered in call history tab of dashboard, and you can also manually download and check against the transcript to view the knowledge base retrieval results. |
| `latency` | object | Latency tracking of the call, available after call ends. Not all fields here will be available, as it depends on the type of call and feature used. |
| `latency.asr` | object |  |
| `latency.asr.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.asr.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.asr.num` | number | Number of data points (number of times latency is tracked). |
| `latency.asr.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.asr.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.asr.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.asr.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.asr.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.e2e` | object |  |
| `latency.e2e.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.e2e.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.e2e.num` | number | Number of data points (number of times latency is tracked). |
| `latency.e2e.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.e2e.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.e2e.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.e2e.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.e2e.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.knowledgeBase` | object |  |
| `latency.knowledgeBase.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.knowledgeBase.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.knowledgeBase.num` | number | Number of data points (number of times latency is tracked). |
| `latency.knowledgeBase.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.knowledgeBase.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.knowledgeBase.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.knowledgeBase.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.knowledgeBase.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.llm` | object |  |
| `latency.llm.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.llm.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.llm.num` | number | Number of data points (number of times latency is tracked). |
| `latency.llm.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.llm.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.llm.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.llm.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.llm.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt` | object |  |
| `latency.llmWebsocketNetworkRtt.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.num` | number | Number of data points (number of times latency is tracked). |
| `latency.llmWebsocketNetworkRtt.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.s2s` | object |  |
| `latency.s2s.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.s2s.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.s2s.num` | number | Number of data points (number of times latency is tracked). |
| `latency.s2s.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.s2s.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.s2s.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.s2s.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.s2s.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.tts` | object |  |
| `latency.tts.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.tts.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.tts.num` | number | Number of data points (number of times latency is tracked). |
| `latency.tts.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.tts.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.tts.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.tts.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.tts.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `llmTokenUsage` | object | LLM token usage of the call, available after call ends. Not populated if using custom LLM, realtime API, or no LLM call is made. |
| `llmTokenUsage.average` | number | Average token count of the call. |
| `llmTokenUsage.numRequests` | number | Number of requests made to the LLM. |
| `llmTokenUsage.values` | array<number> | All the token count values in the call. |
| `metadata` | object | An arbitrary object for storage purpose only. You can put anything here like your internal customer id associated with the call. Not used for processing. You can later get this field from the call object. |
| `optInSignedUrl` | boolean | Whether this agent opts in for signed URLs for public logs and recordings. When enabled, the generated URLs will include security signatures that restrict access and automatically expire after 24 hours. |
| `publicLogUrl` | string | Public log of the call, containing details about all the requests and responses received in LLM WebSocket, latency tracking for each turntaking, helpful for debugging and tracing. Available after call ends. |
| `recordingMultiChannelUrl` | string | Recording of the call, with each party's audio stored in a separate channel. Available after the call ends. |
| `recordingUrl` | string | Recording of the call. Available after call ends. |
| `retellLlmDynamicVariables` | object | Add optional dynamic variables in key value pairs of string that injects into your Response Engine prompt and tool description. Only applicable for Response Engine. |
| `scrubbedRecordingMultiChannelUrl` | string | Recording of the call without PII, with each party's audio stored in a separate channel. Available after the call ends. |
| `scrubbedRecordingUrl` | string | Recording of the call without PII. Available after call ends. |
| `scrubbedTranscriptWithToolCalls` | array<object> | Transcript of the call weaved with tool call invocation and results, without PII. It precisely captures when (at what utterance, which word) the tool was invoked and what was the result. Available after call ends. |
| `scrubbedTranscriptWithToolCalls[].content` | string | Transcript of the utterances. |
| `scrubbedTranscriptWithToolCalls[].role` | string | Documents whether this utterance is spoken by agent or user. Allowed values: agent, user, transfer_target. |
| `scrubbedTranscriptWithToolCalls[].words` | array<object> | Array of words in the utterance with the word timestamp. Useful for understanding what word was spoken at what time. Note that the word timestamp is not guaranteed to be accurate, it's more like an approximation. |
| `scrubbedTranscriptWithToolCalls[].words[].end` | number | End time of the word in the call in second. This is relative audio time, not wall time. |
| `scrubbedTranscriptWithToolCalls[].words[].start` | number | Start time of the word in the call in second. This is relative audio time, not wall time. |
| `scrubbedTranscriptWithToolCalls[].words[].word` | string | Word transcript (with punctuation if applicable). |
| `startTimestamp` | number | Begin timestamp (milliseconds since epoch) of the call. Available after call starts. |
| `transcript` | string | Transcription of the call. Available after call ends. |
| `transcriptObject` | array<object> | Transcript of the call in the format of a list of utterance, with timestamp. Available after call ends. |
| `transcriptObject[].content` | string | Transcript of the utterances. |
| `transcriptObject[].role` | string | Documents whether this utterance is spoken by agent or user. Allowed values: agent, user, transfer_target. |
| `transcriptObject[].words` | array<object> | Array of words in the utterance with the word timestamp. Useful for understanding what word was spoken at what time. Note that the word timestamp is not guaranteed to be accurate, it's more like an approximation. |
| `transcriptObject[].words[].end` | number | End time of the word in the call in second. This is relative audio time, not wall time. |
| `transcriptObject[].words[].start` | number | Start time of the word in the call in second. This is relative audio time, not wall time. |
| `transcriptObject[].words[].word` | string | Word transcript (with punctuation if applicable). |
| `transcriptWithToolCalls` | array<object> | Transcript of the call weaved with tool call invocation and results. It precisely captures when (at what utterance, which word) the tool was invoked and what was the result. Available after call ends. |
| `transcriptWithToolCalls[].content` | string | Transcript of the utterances. |
| `transcriptWithToolCalls[].role` | string | Documents whether this utterance is spoken by agent or user. Allowed values: agent, user, transfer_target. |
| `transcriptWithToolCalls[].words` | array<object> | Array of words in the utterance with the word timestamp. Useful for understanding what word was spoken at what time. Note that the word timestamp is not guaranteed to be accurate, it's more like an approximation. |
| `transcriptWithToolCalls[].words[].end` | number | End time of the word in the call in second. This is relative audio time, not wall time. |
| `transcriptWithToolCalls[].words[].start` | number | Start time of the word in the call in second. This is relative audio time, not wall time. |
| `transcriptWithToolCalls[].words[].word` | string | Word transcript (with punctuation if applicable). |
| `transferDestination` | string | The destination number or identifier where the call was transferred to. Only populated when the disconnection reason was `call_transfer`. Can be a phone number or a SIP URI. SIP URIs are prefixed with "sip:" and may include a ";transport=..." portion (if transport is known) where the transport type can be "tls", "tcp" or "udp". |
| `transferEndTimestamp` | number | Transfer end timestamp (milliseconds since epoch) of the call. Available after transfer call ends. |

## Native endpoint

Through the native Retell AI API, this operation is `POST /v2/list-calls` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

