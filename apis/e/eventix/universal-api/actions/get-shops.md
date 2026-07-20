# Eventix: Get Shops

Retrieves shops from Eventix.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shops
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shops?connectionId=$CONNECTION_ID&type=normal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "normal"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shops?${params}`, {
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
| `type` | list<string> | yes | How to handle archived Shops. One of: `0`, `1`, `2`. Default: `normal`. Example: `normal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_prune": true,
      "company_terms": "string",
      "currency": "string",
      "description": "string",
      "email_must_be_unique": true,
      "email_validation_rule": "ava@example.com",
      "event_selection": "string",
      "facebook_page_url": "https://example.com",
      "global_terms": "string",
      "guid": "string",
      "max_tickets_per_order": 1,
      "name": "Ava Chen",
      "reservation_time": 1,
      "seats_public_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_prune` | boolean |  |
| `company_terms` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `email_must_be_unique` | boolean |  |
| `email_validation_rule` | string |  |
| `event_selection` | string |  |
| `facebook_page_url` | string |  |
| `global_terms` | string |  |
| `guid` | string |  |
| `max_tickets_per_order` | number |  |
| `name` | string |  |
| `reservation_time` | number |  |
| `seats_public_key` | string |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/shop/:type` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shops.md) for the provider-specific parameters and requirements.

