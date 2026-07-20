# Prembly: Get Verification Status

Retrieves a verification status from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-verification-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-verification-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-verification-status?${params}`, {
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
      "billing_status": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "endpoint_name": "Ava Chen",
      "endpoint": {
        "code": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "organisation": "string",
      "organisation_name": "Ava Chen",
      "price": "string",
      "product": "string",
      "reference": "string",
      "request_data": "string",
      "response_code": "string",
      "response_data": "string",
      "source": "string",
      "verification_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_status` | boolean |  |
| `created_at` | date |  |
| `endpoint_name` | string |  |
| `endpoint.code` | string |  |
| `endpoint.id` | string |  |
| `endpoint.name` | string |  |
| `organisation` | string |  |
| `organisation_name` | string |  |
| `price` | string |  |
| `product` | string |  |
| `reference` | string |  |
| `request_data` | string |  |
| `response_code` | string |  |
| `response_data` | string |  |
| `source` | string |  |
| `verification_status` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /verification/:id/status` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-status.md) for the provider-specific parameters and requirements.

