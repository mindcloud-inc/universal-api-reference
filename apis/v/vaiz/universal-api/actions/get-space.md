# Vaiz: Get Space

Retrieves the current space from Vaiz.

```
GET https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/get-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/get-space?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/get-space?${params}`, {
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
      "space": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `space` | object |  |

## Native endpoint

Through the native Vaiz API, this operation is `POST getSpace` (base URL `https://api.vaiz.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space.md) for the provider-specific parameters and requirements.

