# pretix: List Item Variations

Retrieves item variations from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-item-variations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-item-variations?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string&event=string&item=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizer": "string",
  "event": "string",
  "item": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-item-variations?${params}`, {
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
| `item` | string | yes | pretix item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "allSalesChannels": true,
      "availableFrom": "string",
      "availableUntil": "string",
      "checkinAttention": true,
      "checkinText": "string",
      "defaultPrice": "string",
      "description": {},
      "id": 1,
      "limitSalesChannels": [
        "string"
      ],
      "position": 1,
      "price": "string",
      "requireApproval": true,
      "requireMembership": true,
      "requireMembershipTypes": [
        1
      ],
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `allSalesChannels` | boolean |  |
| `availableFrom` | string |  |
| `availableUntil` | string |  |
| `checkinAttention` | boolean |  |
| `checkinText` | string |  |
| `defaultPrice` | string |  |
| `description` | object |  |
| `id` | number |  |
| `limitSalesChannels[]` | string |  |
| `position` | number |  |
| `price` | string |  |
| `requireApproval` | boolean |  |
| `requireMembership` | boolean |  |
| `requireMembershipTypes[]` | number |  |
| `value` | object |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/items/:item/variations/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-item-variations.md) for the provider-specific parameters and requirements.

