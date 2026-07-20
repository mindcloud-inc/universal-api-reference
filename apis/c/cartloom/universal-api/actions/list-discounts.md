# Cartloom: List Discounts

Retrieves multiple discount records from Cartloom.

```
GET https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/list-discounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cartloom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/list-discounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/list-discounts?${params}`, {
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
      "enabled": "string",
      "id": "string",
      "title": "string",
      "used": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | string | Whether the discount is enabled. |
| `id` | string | Discount ID. |
| `title` | string | Discount title. |
| `used` | string | Usage/code value returned by Cartloom in the list response. |

## Native endpoint

Through the native Cartloom API, this operation is `POST /discounts/list/format/json` (base URL `https://mindcloudstage0424.cartloom.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-discounts.md) for the provider-specific parameters and requirements.

