# Celigo: List Connections



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-connections?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no | Only return connections with this exact external identifier. |
| `fetchQueueSize` | boolean | no | Include queue size information for each connection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assistant": "string",
      "autoRecoverRateLimitErrors": true,
      "connectorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "debugDate": "2026-05-07T12:00:00.000Z",
      "debugUntil": "2026-05-07T12:00:00.000Z",
      "enableCsvObjectParsing": true,
      "enableMicroBatchForOneToMany": true,
      "ftp": {},
      "http": {},
      "id": "string",
      "integrationId": "string",
      "isHTTP": true,
      "lastModified": "2026-05-07T12:00:00.000Z",
      "microServices": {},
      "name": "Ava Chen",
      "netsuite": {},
      "offline": true,
      "rest": {},
      "sandbox": true,
      "settings": {},
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
| `assistant` | string |  |
| `autoRecoverRateLimitErrors` | boolean |  |
| `connectorId` | string |  |
| `createdAt` | date |  |
| `debugDate` | date |  |
| `debugUntil` | date |  |
| `enableCsvObjectParsing` | boolean |  |
| `enableMicroBatchForOneToMany` | boolean |  |
| `ftp` | object |  |
| `http` | object |  |
| `id` | string |  |
| `integrationId` | string |  |
| `isHTTP` | boolean |  |
| `lastModified` | date |  |
| `microServices` | object |  |
| `name` | string |  |
| `netsuite` | object |  |
| `offline` | boolean |  |
| `rest` | object |  |
| `sandbox` | boolean |  |
| `settings` | object |  |
| `sourceId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /connections` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-connections.md) for the provider-specific parameters and requirements.

