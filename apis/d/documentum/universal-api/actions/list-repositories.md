# Documentum: List Repositories



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-repositories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-repositories?${params}`, {
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
      "entries": [
        {}
      ],
      "id": "string",
      "links": [
        {}
      ],
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | Repository entries returned by the Documentum repositories feed. |
| `id` | string | Feed/resource identifier. |
| `links` | array<object> | Hypermedia links returned by Documentum REST. |
| `title` | string | Feed title. |
| `updated` | date | Last-updated timestamp from the repository feed. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-repositories.md) for the provider-specific parameters and requirements.

