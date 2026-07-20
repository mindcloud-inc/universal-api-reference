# Raven Tools: List Website Types

Retrieves website types from Raven Tools.

```
GET https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-website-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-website-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-website-types?${params}`, {
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
      "results": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<string> | Available Raven website types. |

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-website-types.md) for the provider-specific parameters and requirements.

