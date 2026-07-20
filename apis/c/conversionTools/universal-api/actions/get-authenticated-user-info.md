# Conversion Tools: Get Authenticated User Info

Retrieves authenticated user info from Conversion Tools.

```
GET https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-authenticated-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conversion Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-authenticated-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-authenticated-user-info?${params}`, {
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
      "error": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Authenticated Conversion Tools account email. |
| `error` | string | Provider error message when present. |

## Native endpoint

Through the native Conversion Tools API, this operation is `GET /auth` (base URL `https://api.conversiontools.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user-info.md) for the provider-specific parameters and requirements.

