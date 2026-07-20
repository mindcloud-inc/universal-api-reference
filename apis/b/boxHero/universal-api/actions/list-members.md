# BoxHero: List Members

Retrieves team members from BoxHero.

```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-members?${params}`, {
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
      "items": [
        {
          "id": 1,
          "name": "Ava Chen",
          "role": "string"
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
| `items[].id` | number |  |
| `items[].name` | string |  |
| `items[].role` | string |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/members` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

