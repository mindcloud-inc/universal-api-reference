# Certs 365: List Issuers

Retrieves issuer details from Certs 365.

```
GET https://connect.mindcloud.co/v1/universal/certs365/latest/actions/list-issuers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/list-issuers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certs365/latest/actions/list-issuers?${params}`, {
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
      "activeIssuers": 1,
      "allIssuers": 1,
      "code": 1,
      "data": [
        {}
      ],
      "inactiveIssuers": 1,
      "message": "string",
      "pendingIssuers": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeIssuers` | number |  |
| `allIssuers` | number |  |
| `code` | number |  |
| `data` | array<object> |  |
| `inactiveIssuers` | number |  |
| `message` | string |  |
| `pendingIssuers` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `GET /api/get-all-issuers/` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issuers.md) for the provider-specific parameters and requirements.

