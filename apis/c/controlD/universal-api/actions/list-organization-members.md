# Control D: List Organization Members

Retrieves organization members from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-organization-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-organization-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-organization-members?${params}`, {
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
      "email": "ava@example.com",
      "last_active": 1,
      "permission": {},
      "PK": "string",
      "status": 1,
      "twofa": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `last_active` | number |  |
| `permission` | object |  |
| `PK` | string |  |
| `status` | number |  |
| `twofa` | number |  |

## Native endpoint

Through the native Control D API, this operation is `GET /organizations/members` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-members.md) for the provider-specific parameters and requirements.

