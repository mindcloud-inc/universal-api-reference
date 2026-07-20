# WebinarGeek: List Webinars



```
GET https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/list-webinars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebinarGeek `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/list-webinars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/list-webinars?${params}`, {
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
      "archived": true,
      "createdAt": 1,
      "id": 1,
      "language": "string",
      "ondemand": true,
      "title": "string",
      "url": "https://example.com",
      "viewWithoutRegistrationUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | number |  |
| `id` | number |  |
| `language` | string |  |
| `ondemand` | boolean |  |
| `title` | string |  |
| `url` | string |  |
| `viewWithoutRegistrationUrl` | string |  |

## Native endpoint

Through the native WebinarGeek API, this operation is `GET /webinars` (base URL `https://app.webinargeek.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webinars.md) for the provider-specific parameters and requirements.

