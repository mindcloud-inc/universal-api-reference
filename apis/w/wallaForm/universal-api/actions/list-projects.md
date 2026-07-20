# Walla Form: List Projects



```
GET https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walla Form `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/list-projects?connectionId=$CONNECTION_ID&workspaceKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/list-projects?${params}`, {
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
| `workspaceKey` | string | yes | The Walla workspace key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true,
      "bgColor": "string",
      "brandLogoUrl": "https://example.com",
      "closeDateTime": "2026-05-07T12:00:00.000Z",
      "displayTitle": "string",
      "emoji": "string",
      "enableCloseScheduling": true,
      "enableOpenScheduling": true,
      "enableResponseLimit": true,
      "hiddenFields": [
        {}
      ],
      "isDeployed": true,
      "key": "string",
      "metadata": {},
      "openDateTime": "2026-05-07T12:00:00.000Z",
      "responseLimit": 1,
      "responseNumber": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |
| `bgColor` | string |  |
| `brandLogoUrl` | string |  |
| `closeDateTime` | date |  |
| `displayTitle` | string |  |
| `emoji` | string |  |
| `enableCloseScheduling` | boolean |  |
| `enableOpenScheduling` | boolean |  |
| `enableResponseLimit` | boolean |  |
| `hiddenFields` | array<object> |  |
| `isDeployed` | boolean |  |
| `key` | string |  |
| `metadata` | object |  |
| `openDateTime` | date |  |
| `responseLimit` | number |  |
| `responseNumber` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Walla Form API, this operation is `GET /workspace/:workspaceKey/project/list` (base URL `https://walla-api.data-lab.workers.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

