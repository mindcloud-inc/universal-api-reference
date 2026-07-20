# VdoCipher: List Policies

Lists policies in VdoCipher.

```
GET https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-policies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-policies?${params}`, {
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
      "policies": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `policies` | array<object> |  |

## Native endpoint

Through the native VdoCipher API, this operation is `GET /policy` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-policies.md) for the provider-specific parameters and requirements.

