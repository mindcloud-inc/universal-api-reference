# ClustDoc: List Text Data Fields



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-text-data-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-text-data-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-text-data-fields?${params}`, {
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
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "parent_type": "string",
      "rank": 1,
      "slug": "string",
      "team_id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `parent_type` | string |  |
| `rank` | number |  |
| `slug` | string |  |
| `team_id` | number |  |
| `type` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /data-fields` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-text-data-fields.md) for the provider-specific parameters and requirements.

