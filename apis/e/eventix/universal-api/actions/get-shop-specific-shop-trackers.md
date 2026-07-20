# Eventix: Get attached ShopTrackers of Shop

Retrieves shop trackers for an Eventix shop.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-shop-trackers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-shop-trackers?connectionId=$CONNECTION_ID&guid=shop-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "shop-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-shop-trackers?${params}`, {
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
| `guid` | string | yes | The guid of the Shop. Example: `shop-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "extra_url_parameters": "https://example.com",
      "guid": "string",
      "name": "Ava Chen",
      "shop_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `code` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `extra_url_parameters` | string |  |
| `guid` | string |  |
| `name` | string |  |
| `shop_id` | string |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/shop/:guid/trackers` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shop-specific-shop-trackers.md) for the provider-specific parameters and requirements.

