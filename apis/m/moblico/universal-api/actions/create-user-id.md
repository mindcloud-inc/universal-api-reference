# Moblico: Create User ID



```
GET https://connect.mindcloud.co/v1/universal/moblico/latest/actions/create-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moblico `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moblico/latest/actions/create-user-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moblico/latest/actions/create-user-id?${params}`, {
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
      "UUID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `UUID` | string | Generated unique Moblico user ID. |

## Native endpoint

Through the native Moblico API, this operation is `GET /users/createId` (base URL `https://moblico.net/services/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-id.md) for the provider-specific parameters and requirements.

