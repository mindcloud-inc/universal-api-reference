# Celigo: List Integrations



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-integrations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-integrations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "apiGroupings": [
        "string"
      ],
      "changeEditionSteps": [
        "string"
      ],
      "connectorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "flowGroupings": [
        {}
      ],
      "id": "string",
      "install": [
        {}
      ],
      "installSteps": [
        {}
      ],
      "lastModified": "2026-05-07T12:00:00.000Z",
      "mode": "string",
      "name": "Ava Chen",
      "registeredConnectionIds": [
        "string"
      ],
      "registeredLookupCacheIds": [
        "string"
      ],
      "sandbox": true,
      "settings": {},
      "sourceId": "string",
      "templateId": "string",
      "uninstallSteps": [
        "string"
      ],
      "updateInProgress": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiGroupings` | array |  |
| `changeEditionSteps` | array |  |
| `connectorId` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `flowGroupings` | array<object> |  |
| `id` | string |  |
| `install` | array<object> |  |
| `installSteps` | array<object> |  |
| `lastModified` | date |  |
| `mode` | string |  |
| `name` | string |  |
| `registeredConnectionIds` | array<string> |  |
| `registeredLookupCacheIds` | array |  |
| `sandbox` | boolean |  |
| `settings` | object |  |
| `sourceId` | string |  |
| `templateId` | string |  |
| `uninstallSteps` | array |  |
| `updateInProgress` | boolean |  |
| `version` | string |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /integrations` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.

