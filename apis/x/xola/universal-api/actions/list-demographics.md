# Xola: List Demographics

Finds demographics in Xola.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-demographics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-demographics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-demographics?${params}`, {
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
      "data": [
        [
          {}
        ]
      ],
      "paging": {
        "next": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> | Demographic records returned by Xola. |
| `data[].discount.amount` | number | Discount amount. |
| `data[].discount.amountType` | string | Discount amount type. |
| `data[].experience.id` | string | Associated experience identifier. |
| `data[].id` | string | Demographic identifier. |
| `data[].label` | string | Display label. |
| `data[].object` | string | Xola object type. |
| `data[].parent.id` | string | Parent demographic identifier. |
| `data[].seller.id` | string | Owning seller identifier. |
| `paging.next` | string | Cursor for the next page. |

## Native endpoint

Through the native Xola API, this operation is `GET /demographics` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-demographics.md) for the provider-specific parameters and requirements.

