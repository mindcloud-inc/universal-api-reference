# SimpleLocalize: List Project Activity

Retrieves project activity from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-project-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-project-activity?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-project-activity?${params}`, {
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
      "environment": {},
      "id": "string",
      "numberOfChanges": 1,
      "numberOfKeys": 1,
      "numberOfLanguages": 1,
      "running": true,
      "source": "string",
      "type": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `environment` | object |  |
| `id` | string |  |
| `numberOfChanges` | number |  |
| `numberOfKeys` | number |  |
| `numberOfLanguages` | number |  |
| `running` | boolean |  |
| `source` | string |  |
| `type` | string |  |
| `user` | string |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v1/activity` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-activity.md) for the provider-specific parameters and requirements.

