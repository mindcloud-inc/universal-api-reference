# DirectIQ: Get a template

Retrieves a template from DirectIQ by ID.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-template?${params}`, {
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
      "createdDate": "2026-05-07T12:00:00.000Z",
      "html": "string",
      "id": 1,
      "isFavorite": true,
      "jsonData": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "subject": "string",
      "templateTags": [
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
| `createdDate` | date |  |
| `html` | string |  |
| `id` | number |  |
| `isFavorite` | boolean |  |
| `jsonData` | string |  |
| `lastModified` | date |  |
| `name` | string |  |
| `subject` | string |  |
| `templateTags[]` | array<object> |  |
| `templateTags[].id` | number |  |
| `templateTags[].name` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /core/template/get/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-template.md) for the provider-specific parameters and requirements.

