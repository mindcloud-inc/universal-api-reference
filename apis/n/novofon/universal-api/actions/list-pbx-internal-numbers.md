# Novofon: List PBX Internal Numbers

Retrieves PBX internal numbers from Novofon.

```
GET https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-pbx-internal-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-pbx-internal-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-pbx-internal-numbers?${params}`, {
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
      "numbers": [
        "string"
      ],
      "pbxId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numbers[]` | string |  |
| `pbxId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/pbx/internal/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pbx-internal-numbers.md) for the provider-specific parameters and requirements.

