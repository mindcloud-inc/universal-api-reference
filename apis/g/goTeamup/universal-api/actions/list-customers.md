# GoTeamup: List Customers

Finds customers in GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customers?${params}`, {
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
          "createdAt": "string",
          "email": "ava@example.com",
          "family": {},
          "familyRole": {},
          "firstName": "Ava",
          "id": 1,
          "image": {},
          "isLead": true,
          "isStatusLocked": true,
          "lastName": "Chen",
          "leadSource": {},
          "object": "string",
          "participating": true,
          "provider": 1,
          "referralCode": {
            "code": "string",
            "shareUrl": "https://example.com"
          },
          "status": {},
          "visibility": "string"
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
| `results[].createdAt` | string |  |
| `results[].email` | string |  |
| `results[].family` | object |  |
| `results[].familyRole` | object |  |
| `results[].firstName` | string |  |
| `results[].id` | number |  |
| `results[].image` | object |  |
| `results[].isLead` | boolean |  |
| `results[].isStatusLocked` | boolean |  |
| `results[].lastName` | string |  |
| `results[].leadSource` | object |  |
| `results[].object` | string |  |
| `results[].participating` | boolean |  |
| `results[].provider` | number |  |
| `results[].referralCode.code` | string |  |
| `results[].referralCode.shareUrl` | string |  |
| `results[].status` | object |  |
| `results[].visibility` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /customers` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

