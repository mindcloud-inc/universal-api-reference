# Bookvault: List Roles

Retrieves active roles from your Bookvault account.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-roles?${params}`, {
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
      "Admin": true,
      "Payments": true,
      "PlaceOrders": true,
      "Reporting": true,
      "RoleID": 1,
      "RoleName": "Ava Chen",
      "ViewOrders": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Admin` | boolean |  |
| `Payments` | boolean |  |
| `PlaceOrders` | boolean |  |
| `Reporting` | boolean |  |
| `RoleID` | number |  |
| `RoleName` | string |  |
| `ViewOrders` | boolean |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Roles` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

