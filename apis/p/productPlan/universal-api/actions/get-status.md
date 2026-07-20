# ProductPlan: Get Status

Retrieves application status details from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-status?${params}`, {
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
      "application": "string",
      "generated_at": "2026-05-07T12:00:00.000Z",
      "status": {},
      "user": {},
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | string | API name reported by the ProductPlan status endpoint. |
| `generated_at` | date | Timestamp when the status payload was generated. |
| `status` | object | Nested health information for ProductPlan services. |
| `user` | object | Authenticated ProductPlan user information returned by the status endpoint. |
| `version` | number | API version reported by the ProductPlan status endpoint. |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /status` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status.md) for the provider-specific parameters and requirements.

