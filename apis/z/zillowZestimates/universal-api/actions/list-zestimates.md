# Zillow Zestimates: List zestimates

Retrieves current property, rental, and foreclosure Zestimates from Zillow.

```
GET https://connect.mindcloud.co/v1/universal/zillowZestimates/latest/actions/list-zestimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow Zestimates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowZestimates/latest/actions/list-zestimates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowZestimates/latest/actions/list-zestimates?${params}`, {
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
| `address` | string | no | Street address to look up a Zestimate for a property. Default: `123 Main Street`. |
| `zpidIn` | string | no | Comma-separated list of Zillow property IDs to look up. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "highPercent": 1,
      "houseNumber": "string",
      "id": "string",
      "Latitude": 1,
      "Longitude": 1,
      "lowPercent": 1,
      "postalCode": "string",
      "rentalHighPercent": 1,
      "rentalLowPercent": 1,
      "rentalTimestamp": "2026-05-07T12:00:00.000Z",
      "rentalZestimate": 1,
      "state": "string",
      "streetName": "Ava Chen",
      "streetSuffix": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "unitNumber": "string",
      "zestimate": 1,
      "zillowUrl": "https://example.com",
      "zpid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `BridgeModificationTimestamp` | date |  |
| `city` | string |  |
| `highPercent` | number |  |
| `houseNumber` | string |  |
| `id` | string |  |
| `Latitude` | number |  |
| `Longitude` | number |  |
| `lowPercent` | number |  |
| `postalCode` | string |  |
| `rentalHighPercent` | number |  |
| `rentalLowPercent` | number |  |
| `rentalTimestamp` | date |  |
| `rentalZestimate` | number |  |
| `state` | string |  |
| `streetName` | string |  |
| `streetSuffix` | string |  |
| `timestamp` | date |  |
| `unitNumber` | string |  |
| `zestimate` | number |  |
| `zillowUrl` | string |  |
| `zpid` | string |  |

## Native endpoint

Through the native Zillow Zestimates API, this operation is `GET /zestimates_v2/zestimates` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-zestimates.md) for the provider-specific parameters and requirements.

