# Printify: List Webhooks

Retrieves webhooks from a Printify shop.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&shopId=27141936" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shopId": "27141936"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-webhooks?${params}`, {
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
| `shopId` | number | yes | Printify shop id. Default: `27141936`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "shopId": "string",
      "topic": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `shopId` | string |  |
| `topic` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Printify API, this operation is `GET /shops/:shop_id/webhooks.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

