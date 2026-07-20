# Twenty: List Dashboards



```
GET https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-dashboards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-dashboards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-dashboards?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "deletedAt": "string",
      "id": "string",
      "pageLayoutId": "string",
      "position": 1,
      "searchVector": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {
        "name": "Ava Chen",
        "source": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy.name` | string |  |
| `createdBy.source` | string |  |
| `deletedAt` | string |  |
| `id` | string |  |
| `pageLayoutId` | string |  |
| `position` | number |  |
| `searchVector` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `updatedBy.name` | string |  |
| `updatedBy.source` | string |  |

## Native endpoint

Through the native Twenty API, this operation is `GET /rest/dashboards` (base URL `https://api.twenty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dashboards.md) for the provider-specific parameters and requirements.

