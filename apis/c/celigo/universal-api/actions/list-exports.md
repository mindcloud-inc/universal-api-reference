# Celigo: List Exports



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-exports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-exports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-exports?${params}`, {
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
| `externalId` | string | no | Only return exports with this exact external identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adaptorType": "string",
      "apiIdentifier": "string",
      "asynchronous": true,
      "connectionId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "file": {},
      "filter": {},
      "hooks": {},
      "id": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "mockOutput": {},
      "name": "Ava Chen",
      "netsuite": {},
      "once": {},
      "oneToMany": true,
      "pageSize": 1,
      "rawData": "string",
      "sampleData": "string",
      "sandbox": true,
      "sourceId": "string",
      "transform": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adaptorType` | string |  |
| `apiIdentifier` | string |  |
| `asynchronous` | boolean |  |
| `connectionId` | string |  |
| `createdAt` | date |  |
| `file` | object |  |
| `filter` | object |  |
| `hooks` | object |  |
| `id` | string |  |
| `lastModified` | date |  |
| `mockOutput` | object |  |
| `name` | string |  |
| `netsuite` | object |  |
| `once` | object |  |
| `oneToMany` | boolean |  |
| `pageSize` | number |  |
| `rawData` | string |  |
| `sampleData` | string |  |
| `sandbox` | boolean |  |
| `sourceId` | string |  |
| `transform` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /exports` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-exports.md) for the provider-specific parameters and requirements.

