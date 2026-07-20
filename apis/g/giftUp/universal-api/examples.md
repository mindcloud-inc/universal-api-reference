# Gift Up Universal API Examples

These examples use the MindCloud API key and Gift Up connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-company?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "canShowCheckout": true,
      "currency": "string",
      "id": "string",
      "isCheckoutLive": true,
      "name": "Ava Chen",
      "onboardingCompleted": true
    }
  ],
  "meta": {}
}
```

See the full [Get Company action reference](actions/get-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/giftUp/latest/actions/get-company).

## Create Item



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

Example response:

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

See the full [Create Item action reference](actions/create-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/giftUp/latest/actions/create-item).
