# QStash: Get DLQ Message

Retrieves a dead-letter queue message from QStash.

```
GET https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-dlq-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-dlq-message?connectionId=$CONNECTION_ID&dlqId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dlqId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-dlq-message?${params}`, {
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
| `dlqId` | string | yes | DLQ ID of the message to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `bodyBase64` | string |  |
| `callback` | string |  |
| `callerIP` | string |  |
| `createdAt` | number |  |
| `endpointName` | string |  |
| `failureCallback` | string |  |
| `flowControlKey` | string |  |
| `header` | object |  |
| `label` | string |  |
| `maxRetries` | number |  |
| `messageId` | string |  |
| `method` | string |  |
| `notBefore` | number |  |
| `parallelism` | number |  |
| `period` | number |  |
| `queueName` | string |  |
| `rate` | number |  |
| `responseBody` | string |  |
| `responseBodyBase64` | string |  |
| `responseHeader` | object |  |
| `responseStatus` | number |  |
| `scheduleId` | string |  |
| `topicName` | string |  |
| `url` | string |  |

## Native endpoint

Through the native QStash API, this operation is `GET /v2/dlq/:dlqId` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dlq-message.md) for the provider-specific parameters and requirements.

