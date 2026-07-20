# IssueBadge: List Badges



```
GET https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/list-badges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IssueBadge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/list-badges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/list-badges?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Encrypted badge ID |
| `name` | string | Badge name |

## Native endpoint

Through the native IssueBadge API, this operation is `GET /badge/getall` (base URL `https://app.issuebadge.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-badges.md) for the provider-specific parameters and requirements.

