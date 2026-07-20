# pretix: List Vouchers

Retrieves vouchers from a pretix event.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-vouchers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-vouchers?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizer": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-vouchers?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. |
| `event` | string | yes | pretix event slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowIgnoreQuota": true,
      "blockQuota": true,
      "code": "string",
      "created": "string",
      "id": 1,
      "item": 1,
      "maxUsages": 1,
      "minUsages": 1,
      "priceMode": "string",
      "redeemed": 1,
      "validUntil": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowIgnoreQuota` | boolean |  |
| `blockQuota` | boolean |  |
| `code` | string |  |
| `created` | string |  |
| `id` | number |  |
| `item` | number |  |
| `maxUsages` | number |  |
| `minUsages` | number |  |
| `priceMode` | string |  |
| `redeemed` | number |  |
| `validUntil` | string |  |
| `value` | string |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/vouchers/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vouchers.md) for the provider-specific parameters and requirements.

