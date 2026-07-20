# QStash: List DLQ Messages

Retrieves all dead-letter queue messages from QStash.

```
GET https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-dlq-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-dlq-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-dlq-messages?${params}`, {
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
| `count` | number | no | Number of DLQ messages to return, up to 100. Default: `100`. |
| `cursor` | string | no | Pagination cursor returned by a prior DLQ list response. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseStatus` | number | no | Filter by HTTP response status code of the last delivery attempt. |
| `order` | list | no | Sorting order for DLQ messages. One of: `0`, `1`. Default: `latestFirst`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "messages": [
        {
          "body": "string",
          "bodyBase64": "string",
          "callback": "https://example.com",
          "callerIP": "string",
          "createdAt": 1,
          "endpointName": "Ava Chen",
          "failureCallback": "https://example.com",
          "flowControlKey": "string",
          "header": {},
          "label": "string",
          "maxRetries": 1,
          "messageId": "string",
          "method": "string",
          "notBefore": 1,
          "parallelism": 1,
          "period": 1,
          "queueName": "Ava Chen",
          "rate": 1,
          "responseBody": "string",
          "responseBodyBase64": "string",
          "responseHeader": {},
          "responseStatus": 1,
          "scheduleId": "string",
          "topicName": "Ava Chen",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `messages` | array<object> |  |
| `messages[].body` | string |  |
| `messages[].bodyBase64` | string |  |
| `messages[].callback` | string |  |
| `messages[].callerIP` | string |  |
| `messages[].createdAt` | number |  |
| `messages[].endpointName` | string |  |
| `messages[].failureCallback` | string |  |
| `messages[].flowControlKey` | string |  |
| `messages[].header` | object |  |
| `messages[].label` | string |  |
| `messages[].maxRetries` | number |  |
| `messages[].messageId` | string |  |
| `messages[].method` | string |  |
| `messages[].notBefore` | number |  |
| `messages[].parallelism` | number |  |
| `messages[].period` | number |  |
| `messages[].queueName` | string |  |
| `messages[].rate` | number |  |
| `messages[].responseBody` | string |  |
| `messages[].responseBodyBase64` | string |  |
| `messages[].responseHeader` | object |  |
| `messages[].responseStatus` | number |  |
| `messages[].scheduleId` | string |  |
| `messages[].topicName` | string |  |
| `messages[].url` | string |  |

## Native endpoint

Through the native QStash API, this operation is `GET /v2/dlq` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dlq-messages.md) for the provider-specific parameters and requirements.

