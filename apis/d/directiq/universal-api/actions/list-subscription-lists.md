# DirectIQ: List Subscription Lists

Retrieves subscription lists from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-subscription-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-subscription-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-subscription-lists?${params}`, {
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
      "id": 1,
      "keysMeta": [
        [
          {}
        ]
      ],
      "lastModified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "totalActive": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `keysMeta[]` | array<object> |  |
| `lastModified` | date |  |
| `name` | string |  |
| `totalActive` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /subscription/lists` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscription-lists.md) for the provider-specific parameters and requirements.

