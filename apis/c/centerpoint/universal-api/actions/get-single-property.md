# Centerpoint: Get Property



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-property?connectionId=$CONNECTION_ID&PROPERTY_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PROPERTY_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-property?${params}`, {
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
| `PROPERTY_ID` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[properties]` | string | no | Optional fields properties query parameter. |
| `fields[profiles]` | string | no | Optional fields profiles query parameter. |
| `fields[employees]` | string | no | Optional fields employees query parameter. |
| `fields[companies]` | string | no | Optional fields companies query parameter. |
| `include` | string | no | Optional include query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "accountId": 1,
        "closeRate": {},
        "combinedMeasurement": "string",
        "companyId": 1,
        "county": "string",
        "createdAt": "string",
        "custom": {
          "kkclevel": {},
          "primaryonsitecontact": {},
          "roofaccess": {},
          "stagingandparkinglocation": {}
        },
        "customWithLabels": {
          "maintenancePlanLevel": {},
          "primaryOnsiteContact": {},
          "roofAccess": {},
          "stagingAndParkingLocation": {}
        },
        "deletedAt": {},
        "externalId": "string",
        "importId": {},
        "isVisible": true,
        "latitude": 1,
        "locality": "string",
        "locationId": 1,
        "longitude": 1,
        "managerId": {},
        "name": "Ava Chen",
        "postalCode": "string",
        "primaryBuildingId": 1,
        "primaryContractorId": {},
        "recentActivity": "string",
        "region": "string",
        "squares": 1,
        "streetAddress": "string",
        "subpremise": {},
        "timezone": "string",
        "updatedAt": "string",
        "uuid": "string",
        "weightedAverageScore": {}
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.accountId` | number |  |
| `attributes.closeRate` | object |  |
| `attributes.combinedMeasurement` | string |  |
| `attributes.companyId` | number |  |
| `attributes.county` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.custom.kkclevel` | object |  |
| `attributes.custom.primaryonsitecontact` | object |  |
| `attributes.custom.roofaccess` | object |  |
| `attributes.custom.stagingandparkinglocation` | object |  |
| `attributes.customWithLabels.maintenancePlanLevel` | object |  |
| `attributes.customWithLabels.primaryOnsiteContact` | object |  |
| `attributes.customWithLabels.roofAccess` | object |  |
| `attributes.customWithLabels.stagingAndParkingLocation` | object |  |
| `attributes.deletedAt` | object |  |
| `attributes.externalId` | string |  |
| `attributes.importId` | object |  |
| `attributes.isVisible` | boolean |  |
| `attributes.latitude` | number |  |
| `attributes.locality` | string |  |
| `attributes.locationId` | number |  |
| `attributes.longitude` | number |  |
| `attributes.managerId` | object |  |
| `attributes.name` | string |  |
| `attributes.postalCode` | string |  |
| `attributes.primaryBuildingId` | number |  |
| `attributes.primaryContractorId` | object |  |
| `attributes.recentActivity` | string |  |
| `attributes.region` | string |  |
| `attributes.squares` | number |  |
| `attributes.streetAddress` | string |  |
| `attributes.subpremise` | object |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.uuid` | string |  |
| `attributes.weightedAverageScore` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET properties/:PROPERTY_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-property.md) for the provider-specific parameters and requirements.

