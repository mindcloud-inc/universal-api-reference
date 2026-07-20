# Leantime: Get Project



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-project?connectionId=$CONNECTION_ID&params.id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-project?${params}`, {
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
| `params.id` | number | yes | The project ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": {},
      "clientId": 1,
      "clientName": {},
      "cover": {},
      "details": "string",
      "dollarBudget": 1,
      "end": {},
      "hourBudget": "string",
      "id": 1,
      "isFavorite": 1,
      "menuType": "string",
      "modified": "string",
      "name": "Ava Chen",
      "parent": {},
      "psettings": "string",
      "start": {},
      "state": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | object |  |
| `clientId` | number |  |
| `clientName` | object |  |
| `cover` | object |  |
| `details` | string |  |
| `dollarBudget` | number |  |
| `end` | object |  |
| `hourBudget` | string |  |
| `id` | number |  |
| `isFavorite` | number |  |
| `menuType` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `parent` | object |  |
| `psettings` | string |  |
| `start` | object |  |
| `state` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

