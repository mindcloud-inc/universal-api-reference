# Storyblok: List Datasources

Retrieves datasources from the current Storyblok space.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-datasources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-datasources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-datasources?${params}`, {
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
      "cv": 1,
      "datasources": [
        {
          "id": 1,
          "name": "Ava Chen",
          "slug": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cv` | number | The cache version. |
| `datasources` | array<object> | Available datasources. |
| `datasources[].id` | number | The datasource ID. |
| `datasources[].name` | string | The datasource name. |
| `datasources[].slug` | string | The datasource slug. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /datasources` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-datasources.md) for the provider-specific parameters and requirements.

