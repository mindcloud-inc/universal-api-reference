# NetExplorer: Get File Timeline



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-file-by-file-id-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-file-by-file-id-timeline?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-file-by-file-id-timeline?${params}`, {
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
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "users": [
          "string"
        ],
        "usersCount": 1
      },
      "date": "2026-05-07T12:00:00.000Z",
      "env": "string",
      "extended": [
        {
          "data": "string",
          "date": "2026-05-07T12:00:00.000Z",
          "env": "string",
          "geo": "string",
          "id": 1,
          "owner": "string",
          "ownerId": 1,
          "type": 1
        }
      ],
      "geo": "string",
      "id": 1,
      "owner": "string",
      "ownerId": 1,
      "subtype": 1,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.users` | array<string> |  |
| `data.usersCount` | number |  |
| `date` | date |  |
| `env` | string |  |
| `extended` | array<object> |  |
| `extended[].data` | string |  |
| `extended[].date` | date |  |
| `extended[].env` | string |  |
| `extended[].geo` | string |  |
| `extended[].id` | number |  |
| `extended[].owner` | string |  |
| `extended[].ownerId` | number |  |
| `extended[].type` | number |  |
| `geo` | string |  |
| `id` | number |  |
| `owner` | string |  |
| `ownerId` | number |  |
| `subtype` | number |  |
| `type` | number |  |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /file/:fileId/timeline` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-by-file-id-timeline.md) for the provider-specific parameters and requirements.

