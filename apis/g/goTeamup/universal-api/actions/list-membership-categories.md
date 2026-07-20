# GoTeamup: List Membership Categories

Finds membership categories in GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-membership-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-membership-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-membership-categories?${params}`, {
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
      "count": 1,
      "next": {},
      "previous": {},
      "results": [
        {
          "id": 1,
          "name": "Ava Chen",
          "object": "string",
          "order": 1
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
| `count` | number |  |
| `next` | object |  |
| `previous` | object |  |
| `results[].id` | number |  |
| `results[].name` | string |  |
| `results[].object` | string |  |
| `results[].order` | number |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /membership_categories` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-membership-categories.md) for the provider-specific parameters and requirements.

