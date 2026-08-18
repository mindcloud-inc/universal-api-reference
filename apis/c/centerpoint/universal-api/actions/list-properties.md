# Centerpoint: List Properties



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-properties?${params}`, {
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
| `sort` | string | no | An special argument to sort by selected attribute, use no opperators for ascending order and a minus operator for descending order and input the attribute next to it. e.g. "-createdAt" |
| `filter[updated_at][gt]` | string | no |  |
| `include` | string | no | e.g. = manager,company,primaryContractor,location,integrationRelations |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "accountId": 1,
            "closeRate": "string",
            "combinedMeasurement": "string",
            "companyId": 1,
            "county": "string",
            "createdAt": "string",
            "deletedAt": {},
            "externalId": "string",
            "importId": {},
            "isVisible": true,
            "latitude": 1,
            "locality": "string",
            "locationId": 1,
            "longitude": 1,
            "managerId": 1,
            "name": "Ava Chen",
            "options": {
              "serviceWorkInstructions": "string"
            },
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
            "weightedAverageScore": "string"
          },
          "id": "string",
          "type": "string"
        }
      ],
      "meta": {
        "page": {
          "currentPage": 1,
          "from": 1,
          "lastPage": 1,
          "perPage": 1,
          "to": 1,
          "total": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].attributes.accountId` | number |  |
| `data[].attributes.closeRate` | string |  |
| `data[].attributes.combinedMeasurement` | string |  |
| `data[].attributes.companyId` | number |  |
| `data[].attributes.county` | string |  |
| `data[].attributes.createdAt` | string |  |
| `data[].attributes.deletedAt` | object |  |
| `data[].attributes.externalId` | string |  |
| `data[].attributes.importId` | object |  |
| `data[].attributes.isVisible` | boolean |  |
| `data[].attributes.latitude` | number |  |
| `data[].attributes.locality` | string |  |
| `data[].attributes.locationId` | number |  |
| `data[].attributes.longitude` | number |  |
| `data[].attributes.managerId` | number |  |
| `data[].attributes.name` | string |  |
| `data[].attributes.options.serviceWorkInstructions` | string |  |
| `data[].attributes.postalCode` | string |  |
| `data[].attributes.primaryBuildingId` | number |  |
| `data[].attributes.primaryContractorId` | object |  |
| `data[].attributes.recentActivity` | string |  |
| `data[].attributes.region` | string |  |
| `data[].attributes.squares` | number |  |
| `data[].attributes.streetAddress` | string |  |
| `data[].attributes.subpremise` | object |  |
| `data[].attributes.timezone` | string |  |
| `data[].attributes.updatedAt` | string |  |
| `data[].attributes.uuid` | string |  |
| `data[].attributes.weightedAverageScore` | string |  |
| `data[].id` | string |  |
| `data[].type` | string |  |
| `meta.page.currentPage` | number |  |
| `meta.page.from` | number |  |
| `meta.page.lastPage` | number |  |
| `meta.page.perPage` | number |  |
| `meta.page.to` | number |  |
| `meta.page.total` | number |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET properties` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

