# Codemagic: Get Meta Information

Retrieves Codemagic meta information and public IP addresses.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-meta-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-meta-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-meta-information?${params}`, {
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
      "address_prefixes": [
        "string"
      ],
      "simulator_address_prefixes": [
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
| `address_prefixes` | array<string> |  |
| `simulator_address_prefixes` | array<string> |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/meta` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meta-information.md) for the provider-specific parameters and requirements.

