# Monta: List AFIR Charge Points

Retrieves AFIR-compliant charge points from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-afir-charge-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-afir-charge-points?connectionId=$CONNECTION_ID&country=BE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "BE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-afir-charge-points?${params}`, {
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
| `country` | list<string> | yes | ISO 3166-1 alpha-2 country code. Supported values are DK and BE. One of: `BE`, `DK`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | AFIR page number to retrieve. This endpoint starts at page 1. Default: `1`. |
| `perPage` | number | no | Number of AFIR results per page, up to 1000. Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "energyInfrastructureTable": [
        {
          "energyInfrastructureSite": [
            {
              "dedicatedParkingSpaces": [
                {
                  "amenities": {
                    "lighting": true,
                    "roofed": true
                  },
                  "numberOfSpaces": 1
                }
              ],
              "energyInfrastructureStation": [
                {
                  "numberOfRefillPoints": 1,
                  "refillPoint": [
                    {
                      "idG": "string"
                    }
                  ],
                  "totalMaximumPower": 1
                }
              ],
              "idG": "string",
              "name": {
                "values": [
                  {
                    "lang": "Ava Chen",
                    "value": "Ava Chen"
                  }
                ]
              },
              "typeOfSite": {
                "value": "string"
              }
            }
          ],
          "idG": "string",
          "versionG": "string"
        }
      ],
      "lang": "string",
      "meta": {
        "page": 1,
        "perPage": 1,
        "total": 1
      },
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
| `energyInfrastructureTable[].energyInfrastructureSite[].dedicatedParkingSpaces[].amenities.lighting` | boolean |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].dedicatedParkingSpaces[].amenities.roofed` | boolean |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].dedicatedParkingSpaces[].numberOfSpaces` | number |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].energyInfrastructureStation[].numberOfRefillPoints` | number |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].energyInfrastructureStation[].refillPoint[].idG` | string |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].energyInfrastructureStation[].totalMaximumPower` | number |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].idG` | string |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].name.values[].lang` | string |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].name.values[].value` | string |  |
| `energyInfrastructureTable[].energyInfrastructureSite[].typeOfSite.value` | string |  |
| `energyInfrastructureTable[].idG` | string |  |
| `energyInfrastructureTable[].versionG` | string |  |
| `lang` | string |  |
| `meta.page` | number |  |
| `meta.perPage` | number |  |
| `meta.total` | number |  |
| `publicationCreator.country` | string |  |
| `publicationCreator.nationalIdentifier` | string |  |
| `publicationTime` | date |  |

## Native endpoint

Through the native Monta API, this operation is `GET /afir/charge-points` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-afir-charge-points.md) for the provider-specific parameters and requirements.

