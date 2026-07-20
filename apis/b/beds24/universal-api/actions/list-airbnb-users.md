# Beds24: List Airbnb Users

Retrieves Airbnb user IDs connected to a Beds24 account.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-users?${params}`, {
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
      "airbnbUser": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airbnbUser` | object |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /channels/airbnb/users` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-airbnb-users.md) for the provider-specific parameters and requirements.

