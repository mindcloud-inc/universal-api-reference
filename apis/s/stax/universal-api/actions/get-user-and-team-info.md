# Stax: Get User and Team Info

Retrieves your user and team details from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-user-and-team-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-user-and-team-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-user-and-team-info?${params}`, {
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
      "merchant": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `merchant` | object | Current merchant account details. |
| `user` | object | Current authenticated user details. |

## Native endpoint

Through the native Stax API, this operation is `GET /self` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-and-team-info.md) for the provider-specific parameters and requirements.

