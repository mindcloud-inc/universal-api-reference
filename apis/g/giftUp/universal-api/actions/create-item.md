# Gift Up: Create Item



```
POST https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "price": 1,
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "price": 1,
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `description` | string | no |  |
| `backingType` | string | no | Default: `Currency`. |
| `priceType` | string | no | Default: `Specified`. |
| `price` | number | yes |  |
| `value` | number | yes |  |
| `groupId` | string | no |  |
| `detailsURL` | string | no |  |
| `stockLevel` | number | no |  |
| `perOrderLimit` | number | no |  |
| `additionalTerms` | string | no |  |
| `sku` | string | no |  |
| `codes[]` | array<string> | no |  |
| `codes[]` | array<string> | no |  |
| `codes[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalTerms": "string",
      "artworkUrl": "https://example.com",
      "availableFrom": "2026-05-07T12:00:00.000Z",
      "availableUntil": "2026-05-07T12:00:00.000Z",
      "backingType": "string",
      "codes": [
        "string"
      ],
      "description": "string",
      "detailsURL": "https://example.com",
      "equivalentValuePerUnit": 1,
      "expiresInDays": "2026-05-07T12:00:00.000Z",
      "expiresInMonths": "2026-05-07T12:00:00.000Z",
      "expiresOn": "2026-05-07T12:00:00.000Z",
      "group": "string",
      "groupId": "string",
      "id": "string",
      "maximumPrice": 1,
      "minimumPrice": 1,
      "name": "Ava Chen",
      "overrideExpiry": true,
      "overrideValidFrom": true,
      "perOrderLimit": {},
      "price": 1,
      "priceType": "string",
      "sku": "string",
      "stockLevel": 1,
      "units": 1,
      "validFrom": "2026-05-07T12:00:00.000Z",
      "validFromInDays": "2026-05-07T12:00:00.000Z",
      "validOnDays": [
        "string"
      ],
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalTerms` | string |  |
| `artworkUrl` | string |  |
| `availableFrom` | date |  |
| `availableUntil` | date |  |
| `backingType` | string |  |
| `codes` | array<string> |  |
| `description` | string |  |
| `detailsURL` | string |  |
| `equivalentValuePerUnit` | number |  |
| `expiresInDays` | date |  |
| `expiresInMonths` | date |  |
| `expiresOn` | date |  |
| `group` | string |  |
| `groupId` | string |  |
| `id` | string |  |
| `maximumPrice` | number |  |
| `minimumPrice` | number |  |
| `name` | string |  |
| `overrideExpiry` | boolean |  |
| `overrideValidFrom` | boolean |  |
| `perOrderLimit` | object |  |
| `price` | number |  |
| `priceType` | string |  |
| `sku` | string |  |
| `stockLevel` | number |  |
| `units` | number |  |
| `validFrom` | date |  |
| `validFromInDays` | date |  |
| `validOnDays` | array<string> |  |
| `value` | number |  |

## Native endpoint

Through the native Gift Up API, this operation is `POST /items` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

