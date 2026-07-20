# Fidel API: Link Location to Offer

Links a location to an offer in Fidel API.

```
POST https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/link-location-to-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/link-location-to-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offerId": "string",
  "locationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/link-location-to-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offerId": "string",
    "locationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offerId` | string | yes |  |
| `locationId` | string | yes | Id of the location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "execution": 1,
      "resource": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `execution` | number |  |
| `resource` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Fidel API API, this operation is `POST /offers/:offerId/locations/:locationId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-location-to-offer.md) for the provider-specific parameters and requirements.

