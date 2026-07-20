# Certs 365: Get Organization Details

Retrieves organization details from Certs 365.

```
GET https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-organization-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-organization-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-organization-details?${params}`, {
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
      "code": 1,
      "data": [
        "string"
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<string> |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `GET /api/get-organization-details` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-details.md) for the provider-specific parameters and requirements.

