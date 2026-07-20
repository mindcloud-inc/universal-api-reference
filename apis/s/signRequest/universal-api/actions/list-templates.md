# SignRequest: List Templates



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-templates?${params}`, {
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
      "name": "Ava Chen",
      "signers": [
        [
          {}
        ]
      ],
      "team": {
        "name": "Ava Chen",
        "subdomain": "string",
        "url": "https://example.com"
      },
      "url": "https://example.com",
      "user": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "uuid": "string",
      "who": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `signers[]` | array<object> |  |
| `team` | object |  |
| `team.name` | string |  |
| `team.subdomain` | string |  |
| `team.url` | string |  |
| `url` | string |  |
| `user` | object |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.lastName` | string |  |
| `uuid` | string |  |
| `who` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `GET /templates/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

