# Golemio API: List Parking Tariffs

Finds parking tariffs in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-tariffs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-tariffs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-tariffs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "chargeBands": {
        "charges": {
          "charge": "string",
          "chargeInterval": 1,
          "chargeOrderIndex": 1,
          "chargeType": "string",
          "id": "string",
          "maxIterationsOfCharge": 1,
          "minIterationsOfCharge": 1,
          "periodsOfTime": {
            "dayInWeek": "string",
            "end": "string",
            "ph": "string",
            "start": "string"
          },
          "validFrom": "2026-05-07T12:00:00.000Z",
          "validTo": "2026-05-07T12:00:00.000Z"
        },
        "freeOfCharge": true,
        "lastModifiedAtSource": "2026-05-07T12:00:00.000Z",
        "maximumDuration": 1,
        "paymentMethods": [
          "string"
        ],
        "paymentMode": "string",
        "primarySource": "string",
        "primarySourceId": "string",
        "url": "https://example.com",
        "validFrom": "2026-05-07T12:00:00.000Z",
        "validTo": "2026-05-07T12:00:00.000Z"
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargeBands` | array<object> | Tariff charge bands. |
| `chargeBands.charges` | array<object> | Charge rules within the band. |
| `chargeBands.charges.charge` | string | Charge amount as provided by Golemio. |
| `chargeBands.charges.chargeInterval` | number | Charge interval in seconds. |
| `chargeBands.charges.chargeOrderIndex` | number | Ordering index for charge rules. |
| `chargeBands.charges.chargeType` | string | Type of charge, such as ordinary, minimum, or maximum. |
| `chargeBands.charges.id` | string | Parking charge identifier. |
| `chargeBands.charges.maxIterationsOfCharge` | number | Maximum number of charge iterations, when provided. |
| `chargeBands.charges.minIterationsOfCharge` | number | Minimum number of charge iterations, when provided. |
| `chargeBands.charges.periodsOfTime` | array<object> | Time periods when this charge applies. |
| `chargeBands.charges.periodsOfTime.dayInWeek` | string | Day of week for the tariff period. |
| `chargeBands.charges.periodsOfTime.end` | string | End time for the tariff period. |
| `chargeBands.charges.periodsOfTime.ph` | string | Public-holiday applicability for the tariff period. |
| `chargeBands.charges.periodsOfTime.start` | string | Start time for the tariff period. |
| `chargeBands.charges.validFrom` | date | Start of validity for this charge rule. |
| `chargeBands.charges.validTo` | date | End of validity for this charge rule, when provided. |
| `chargeBands.freeOfCharge` | boolean | Whether this band is free of charge. |
| `chargeBands.lastModifiedAtSource` | date | When the tariff category was last modified at the source. |
| `chargeBands.maximumDuration` | number | Maximum parking duration for this charge band, in seconds when provided. |
| `chargeBands.paymentMethods` | array<string> | Available payment methods for the charge band. |
| `chargeBands.paymentMode` | string | Whether payment occurs before or after parking. |
| `chargeBands.primarySource` | string | Source system for the tariff charge band. |
| `chargeBands.primarySourceId` | string | Source-specific tariff identifier. |
| `chargeBands.url` | string | Provider URL for the charge band, when provided. |
| `chargeBands.validFrom` | date | Start of tariff validity. |
| `chargeBands.validTo` | date | End of tariff validity, when provided. |
| `id` | string | Parking tariff identifier. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v3/parking-tariffs` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-parking-tariffs.md) for the provider-specific parameters and requirements.

