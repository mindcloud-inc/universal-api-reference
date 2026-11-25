# Celigo: List Imports



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-imports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-imports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-imports?${params}`, {
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
| `externalId` | string | no | Only return imports with this exact external identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adaptorType": "string",
      "apiIdentifier": "string",
      "as2": {},
      "connectionId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "distributed": true,
      "ediProfileId": "string",
      "file": {},
      "filter": {},
      "ftp": {},
      "hooks": {},
      "id": "string",
      "inputContext": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "mapping": {},
      "name": "Ava Chen",
      "oneToMany": true,
      "sampleData": {},
      "sandbox": true,
      "sourceId": "string"
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
| `as2` | object |  |
| `connectionId` | string |  |
| `createdAt` | date |  |
| `distributed` | boolean |  |
| `ediProfileId` | string |  |
| `file` | object |  |
| `filter` | object |  |
| `ftp` | object |  |
| `hooks` | object |  |
| `id` | string |  |
| `inputContext` | string |  |
| `lastModified` | date |  |
| `mapping` | object |  |
| `name` | string |  |
| `oneToMany` | boolean |  |
| `sampleData` | object |  |
| `sandbox` | boolean |  |
| `sourceId` | string |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /imports` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-imports.md) for the provider-specific parameters and requirements.

