# pretix: Get Item

Retrieves an item from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-item?connectionId=$CONNECTION_ID&organizer=string&event=string&item=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string",
  "event": "string",
  "item": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-item?${params}`, {
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
      "admission": true,
      "allSalesChannels": true,
      "availableFrom": "string",
      "availableFromMode": "string",
      "availableUntil": "string",
      "availableUntilMode": "string",
      "category": 1,
      "defaultPrice": "string",
      "description": {},
      "freePrice": true,
      "hasVariations": true,
      "id": 1,
      "internalName": "Ava Chen",
      "limitSalesChannels": [
        "string"
      ],
      "name": {},
      "personalized": true,
      "position": 1,
      "requireVoucher": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `admission` | boolean |  |
| `allSalesChannels` | boolean |  |
| `availableFrom` | string |  |
| `availableFromMode` | string |  |
| `availableUntil` | string |  |
| `availableUntilMode` | string |  |
| `category` | number |  |
| `defaultPrice` | string |  |
| `description` | object |  |
| `freePrice` | boolean |  |
| `hasVariations` | boolean |  |
| `id` | number |  |
| `internalName` | string |  |
| `limitSalesChannels[]` | string |  |
| `name` | object |  |
| `personalized` | boolean |  |
| `position` | number |  |
| `requireVoucher` | boolean |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/items/:item/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

