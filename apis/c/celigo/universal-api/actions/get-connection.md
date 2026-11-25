# Celigo: Get Connection



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-connection?connectionId=$CONNECTION_ID&connectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-connection?${params}`, {
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
| `connectionId` | list<string> | yes | Connection. Pick from List Connections. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoRecoverRateLimitErrors": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "debugDate": "2026-05-07T12:00:00.000Z",
      "debugUntil": "2026-05-07T12:00:00.000Z",
      "enableCsvObjectParsing": true,
      "enableMicroBatchForOneToMany": true,
      "id": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "microServices": {},
      "name": "Ava Chen",
      "netsuite": {},
      "offline": true,
      "queues": [
        {}
      ],
      "sandbox": true,
      "sourceId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoRecoverRateLimitErrors` | boolean |  |
| `createdAt` | date |  |
| `debugDate` | date |  |
| `debugUntil` | date |  |
| `enableCsvObjectParsing` | boolean |  |
| `enableMicroBatchForOneToMany` | boolean |  |
| `id` | string |  |
| `lastModified` | date |  |
| `microServices` | object |  |
| `name` | string |  |
| `netsuite` | object |  |
| `offline` | boolean |  |
| `queues` | array<object> |  |
| `sandbox` | boolean |  |
| `sourceId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /connections/:connectionId` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection.md) for the provider-specific parameters and requirements.

