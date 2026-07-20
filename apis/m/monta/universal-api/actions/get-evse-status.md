# Monta: Get EVSE Status

Retrieves dynamic EVSE status from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-evse-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-evse-status?connectionId=$CONNECTION_ID&evseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "evseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-evse-status?${params}`, {
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
| `evseId` | string | yes | OCPI EVSE identifier, for example DK*MON*E100001. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "electricChargingPointStatus": {
        "availabilityStatus": "string",
        "energyRateUpdate": [
          {
            "applicableCurrency": "string",
            "energyRate": [
              {
                "price": 1,
                "priceType": "string",
                "taxIncluded": true,
                "taxRate": 1,
                "unitType": "string"
              }
            ],
            "idG": "string",
            "ratePolicy": "string"
          }
        ],
        "evseId": "string",
        "lastUpdated": "2026-05-07T12:00:00.000Z"
      },
      "lang": "string",
      "publicationCreator": {
        "country": "string",
        "nationalIdentifier": "string"
      },
      "publicationTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `electricChargingPointStatus.availabilityStatus` | string |  |
| `electricChargingPointStatus.energyRateUpdate[].applicableCurrency` | string |  |
| `electricChargingPointStatus.energyRateUpdate[].energyRate[].price` | number |  |
| `electricChargingPointStatus.energyRateUpdate[].energyRate[].priceType` | string |  |
| `electricChargingPointStatus.energyRateUpdate[].energyRate[].taxIncluded` | boolean |  |
| `electricChargingPointStatus.energyRateUpdate[].energyRate[].taxRate` | number |  |
| `electricChargingPointStatus.energyRateUpdate[].energyRate[].unitType` | string |  |
| `electricChargingPointStatus.energyRateUpdate[].idG` | string |  |
| `electricChargingPointStatus.energyRateUpdate[].ratePolicy` | string |  |
| `electricChargingPointStatus.evseId` | string |  |
| `electricChargingPointStatus.lastUpdated` | date |  |
| `lang` | string |  |
| `publicationCreator.country` | string |  |
| `publicationCreator.nationalIdentifier` | string |  |
| `publicationTime` | date |  |

## Native endpoint

Through the native Monta API, this operation is `GET /afir/charge-points/{evseId}/status` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evse-status.md) for the provider-specific parameters and requirements.

