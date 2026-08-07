# Motive: List assets



```
GET https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Motive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-assets?${params}`, {
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
| `name` | string | no | Filter assets by name. |
| `status` | string | no | Filter assets by status. |
| `exactMatch` | boolean | no | Require exact-casing name matches. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asset": {
        "assetGateway": {
          "active": true,
          "id": 1,
          "identifier": "string"
        },
        "availabilityDetails": {
          "availabilityStatus": "string",
          "updatedAt": "string",
          "updatedByUser": {}
        },
        "axle": {},
        "customType": {},
        "gawr": 1,
        "groupIds": [
          1
        ],
        "gvwr": 1,
        "id": 1,
        "leased": {},
        "length": {},
        "lengthMetricUnits": true,
        "licensePlateNumber": {},
        "licensePlateState": {},
        "make": "string",
        "model": "string",
        "name": "Ava Chen",
        "notes": {},
        "status": "string",
        "type": "string",
        "vin": "string",
        "weightMetricUnits": true,
        "year": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset.assetGateway.active` | boolean |  |
| `asset.assetGateway.id` | number |  |
| `asset.assetGateway.identifier` | string |  |
| `asset.availabilityDetails.availabilityStatus` | string |  |
| `asset.availabilityDetails.updatedAt` | string |  |
| `asset.availabilityDetails.updatedByUser` | object |  |
| `asset.axle` | object |  |
| `asset.customType` | object |  |
| `asset.gawr` | number |  |
| `asset.groupIds[]` | number |  |
| `asset.gvwr` | number |  |
| `asset.id` | number |  |
| `asset.leased` | object |  |
| `asset.length` | object |  |
| `asset.lengthMetricUnits` | boolean |  |
| `asset.licensePlateNumber` | object |  |
| `asset.licensePlateState` | object |  |
| `asset.make` | string |  |
| `asset.model` | string |  |
| `asset.name` | string |  |
| `asset.notes` | object |  |
| `asset.status` | string |  |
| `asset.type` | string |  |
| `asset.vin` | string |  |
| `asset.weightMetricUnits` | boolean |  |
| `asset.year` | string |  |

## Native endpoint

Through the native Motive API, this operation is `GET /v1/assets` (base URL `https://api.gomotive.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

