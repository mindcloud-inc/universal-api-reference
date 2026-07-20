# B2B Wave: List Shipping Options

Retrieves shipping options from B2B Wave.

```
GET https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-shipping-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a B2B Wave `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-shipping-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-shipping-options?${params}`, {
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
      "id": 1,
      "is_default": true,
      "name": "Ava Chen",
      "rule_type": "string",
      "show_choice": true,
      "vat_class_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `is_default` | boolean |  |
| `name` | string |  |
| `rule_type` | string |  |
| `show_choice` | boolean |  |
| `vat_class_id` | number |  |

## Native endpoint

Through the native B2B Wave API, this operation is `GET /shipping_options` (base URL `{{credentials.storeUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipping-options.md) for the provider-specific parameters and requirements.

