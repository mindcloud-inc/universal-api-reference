# serviceminder.io: Find Blogs

Finds blogs in ServiceMinder by search term.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/find-blogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/find-blogs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/find-blogs?${params}`, {
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
| `search` | string | no | Blog search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateSearch": "string",
      "idSearch": "string",
      "matches": [
        {}
      ],
      "message": "string",
      "nameSearch": "Ava Chen",
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateSearch` | string |  |
| `idSearch` | string |  |
| `matches` | array<object> |  |
| `message` | string |  |
| `nameSearch` | string |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /blogs/find` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-blogs.md) for the provider-specific parameters and requirements.

