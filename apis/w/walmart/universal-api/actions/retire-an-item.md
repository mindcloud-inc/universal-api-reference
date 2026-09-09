# Walmart: Retire an Item

Permanently retire an item identified by its SKU.

```
DELETE https://connect.mindcloud.co/v1/universal/walmart/latest/actions/retire-an-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/retire-an-item?connectionId=$CONNECTION_ID&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/retire-an-item?${params}`, {
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
| `sku` | string | yes | An arbitrary alphanumeric unique ID, specified by the seller, which identifies each item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalAttributes": {},
      "errors": {},
      "message": "string",
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalAttributes` | object |  |
| `errors` | object |  |
| `message` | string |  |
| `sku` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `DELETE /v3/items/:sku` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retire-an-item.md) for the provider-specific parameters and requirements.

