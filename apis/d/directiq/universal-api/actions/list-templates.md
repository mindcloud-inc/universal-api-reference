# DirectIQ: List Templates

Retrieves all templates from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-templates?${params}`, {
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
      "nextPageToken": "string",
      "templates": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string |  |
| `templates[]` | array<object> |  |
| `templates[].createdDate` | date |  |
| `templates[].html` | string |  |
| `templates[].id` | number |  |
| `templates[].isFavorite` | boolean |  |
| `templates[].jsonData` | string |  |
| `templates[].lastModified` | date |  |
| `templates[].name` | string |  |
| `templates[].subject` | string |  |
| `templates[].templateTags[]` | array<object> |  |
| `templates[].templateTags[].id` | number |  |
| `templates[].templateTags[].name` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /core/template/list` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

