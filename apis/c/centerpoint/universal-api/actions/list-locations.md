# Centerpoint: List Locations



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-locations?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[locations]` | string | no | Optional fields locations query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "accountName": {},
        "country": "string",
        "county": {},
        "createdAt": "string",
        "deletedAt": {},
        "isMain": true,
        "latitude": 1,
        "locality": {},
        "longitude": 1,
        "name": "Ava Chen",
        "options": {
          "autoGenerateExternalIds": true,
          "dailyProgressReportIncludedWork": "string",
          "dailyProgressReportTimeOfDay": "string",
          "isHideProductPriceFromTechnicians": true,
          "materialMarkup": 1,
          "photoSize": 1,
          "taxLabelOverride": "string",
          "taxPercent": 1
        },
        "placeId": {},
        "postalCode": {},
        "region": {},
        "streetAddress": {},
        "subpremise": {},
        "timezone": "string",
        "updatedAt": "string"
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
| `attributes.accountName` | object |  |
| `attributes.country` | string |  |
| `attributes.county` | object |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.isMain` | boolean |  |
| `attributes.latitude` | number |  |
| `attributes.locality` | object |  |
| `attributes.longitude` | number |  |
| `attributes.name` | string |  |
| `attributes.options.autoGenerateExternalIds` | boolean |  |
| `attributes.options.dailyProgressReportIncludedWork` | string |  |
| `attributes.options.dailyProgressReportTimeOfDay` | string |  |
| `attributes.options.isHideProductPriceFromTechnicians` | boolean |  |
| `attributes.options.materialMarkup` | number |  |
| `attributes.options.photoSize` | number |  |
| `attributes.options.taxLabelOverride` | string |  |
| `attributes.options.taxPercent` | number |  |
| `attributes.placeId` | object |  |
| `attributes.postalCode` | object |  |
| `attributes.region` | object |  |
| `attributes.streetAddress` | object |  |
| `attributes.subpremise` | object |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET locations` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

