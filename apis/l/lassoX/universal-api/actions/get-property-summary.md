# Lasso X: Get Property Summary

Retrieves a property summary from Lasso X.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-property-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-property-summary?connectionId=$CONNECTION_ID&property_number=1&municipality=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "property_number": "1",
  "municipality": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-property-summary?${params}`, {
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
| `property_number` | number | yes | Property number. |
| `municipality` | number | yes | Municipality code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buildings": [
        {
          "buildingNumber": 1,
          "buildingUsage": "string",
          "builtYear": 1
        }
      ],
      "oispdfDownloadLink": "https://example.com",
      "plots": [
        {
          "accessAddress": {
            "accessPoint": {
              "latitude": 1,
              "longitude": 1
            },
            "addressText": "string",
            "city": "string"
          }
        }
      ],
      "propertyRelations": [
        {
          "bfeNumber": 1,
          "ownership": {
            "owningPeople": [
              {
                "owningEntity": {
                  "firstName": "Ava",
                  "lastName": "Chen"
                }
              }
            ]
          },
          "ownershipState": "string",
          "ownershipStateCode": 1,
          "propertyNumber": 1,
          "propertyType": "string",
          "propertyTypeCode": 1
        }
      ],
      "technicalInstallations": [
        {
          "classification": "string"
        }
      ],
      "units": [
        {
          "totalArea": 1,
          "unitUsage": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buildings[].buildingNumber` | number |  |
| `buildings[].buildingUsage` | string |  |
| `buildings[].builtYear` | number |  |
| `oispdfDownloadLink` | string |  |
| `plots[].accessAddress.accessPoint.latitude` | number |  |
| `plots[].accessAddress.accessPoint.longitude` | number |  |
| `plots[].accessAddress.addressText` | string |  |
| `plots[].accessAddress.city` | string |  |
| `propertyRelations[].bfeNumber` | number |  |
| `propertyRelations[].ownership.owningPeople[].owningEntity.firstName` | string |  |
| `propertyRelations[].ownership.owningPeople[].owningEntity.lastName` | string |  |
| `propertyRelations[].ownershipState` | string |  |
| `propertyRelations[].ownershipStateCode` | number |  |
| `propertyRelations[].propertyNumber` | number |  |
| `propertyRelations[].propertyType` | string |  |
| `propertyRelations[].propertyTypeCode` | number |  |
| `technicalInstallations[].classification` | string |  |
| `units[].totalArea` | number |  |
| `units[].unitUsage` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /data/bbr/property/summary` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property-summary.md) for the provider-specific parameters and requirements.

