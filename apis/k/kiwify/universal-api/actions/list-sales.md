# Kiwify: List Sales

Retrieves sales from Kiwify.

```
GET https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-sales?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-sales?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no |  |
| `viewFullSaleDetails` | boolean | no |  |
| `paymentMethod` | string | no |  |
| `productId` | string | no |  |
| `affiliateId` | string | no |  |
| `pageSize` | string | no |  |
| `pageNumber` | string | no |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |
| `updatedAtStartDate` | string | no |  |
| `updatedAtEndDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<string> |  |
| `pagination` | object |  |

## Native endpoint

Through the native Kiwify API, this operation is `GET /v1/sales` (base URL `https://public-api.kiwify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

