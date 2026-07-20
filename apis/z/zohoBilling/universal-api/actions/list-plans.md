# Zoho Billing: List Plans



```
GET https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-plans?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-plans?${params}`, {
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
| `filterBy` | string | no | Filter plans by status, for example `PlanStatus.ACTIVE`. |
| `productId` | string | no | Filter plans to one product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "page_context": {
        "applied_filter": "string",
        "custom_fields": [
          [
            {}
          ]
        ],
        "has_more_page": true,
        "page": 1,
        "per_page": 1,
        "sort_column": "string",
        "sort_order": "string"
      },
      "plans": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `page_context` | object |  |
| `page_context.applied_filter` | string |  |
| `page_context.custom_fields[]` | array<object> |  |
| `page_context.has_more_page` | boolean |  |
| `page_context.page` | number |  |
| `page_context.per_page` | number |  |
| `page_context.sort_column` | string |  |
| `page_context.sort_order` | string |  |
| `plans[]` | array<object> |  |

## Native endpoint

Through the native Zoho Billing API, this operation is `GET /plans` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

