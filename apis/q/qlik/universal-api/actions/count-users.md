# Qlik: Count Users

Retrieves the user count for your Qlik tenant.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/count-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/count-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/count-users?${params}`, {
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/users/actions/count` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-users.md) for the provider-specific parameters and requirements.

