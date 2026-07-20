# ClustDoc: Search Forms By Title



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-forms-by-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-forms-by-title?connectionId=$CONNECTION_ID&title=test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "title": "test"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-forms-by-title?${params}`, {
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
| `title` | string | yes | Form title to match. Default: `test`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absolute_path": "string",
      "created_at": "string",
      "form_data": {},
      "id": 1,
      "is_live": true,
      "team_id": 1,
      "title": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absolute_path` | string |  |
| `created_at` | string |  |
| `form_data` | object |  |
| `id` | number |  |
| `is_live` | boolean |  |
| `team_id` | number |  |
| `title` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /forms` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-forms-by-title.md) for the provider-specific parameters and requirements.

