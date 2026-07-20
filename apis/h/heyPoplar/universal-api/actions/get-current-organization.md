# HeyPoplar: Get Current Organization

Retrieves the current organization from HeyPoplar.

```
GET https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-current-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-current-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-current-organization?${params}`, {
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
      "id": "string",
      "mode": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `mode` | string |  |
| `name` | string |  |

## Native endpoint

Through the native HeyPoplar API, this operation is `GET /me` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-organization.md) for the provider-specific parameters and requirements.

