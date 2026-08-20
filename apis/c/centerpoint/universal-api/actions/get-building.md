# Centerpoint: Get Building



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building?connectionId=$CONNECTION_ID&BUILDING_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BUILDING_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building?${params}`, {
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
| `BUILDING_ID` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[properties]` | string | no |  |
| `fields[buildings]` | string | no |  |
| `include` | string | no | e.g. property,divisions,divisions.outlines,divisions.productTemplateTag |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "country": "string",
        "county": "string",
        "createdAt": "string",
        "deletedAt": {},
        "imageId": {},
        "inspectedAt": {},
        "latitude": 1,
        "locality": "string",
        "longitude": 1,
        "placeId": "string",
        "postalCode": "string",
        "propertyId": 1,
        "region": "string",
        "streetAddress": "string",
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
| `attributes.country` | string |  |
| `attributes.county` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.imageId` | object |  |
| `attributes.inspectedAt` | object |  |
| `attributes.latitude` | number |  |
| `attributes.locality` | string |  |
| `attributes.longitude` | number |  |
| `attributes.placeId` | string |  |
| `attributes.postalCode` | string |  |
| `attributes.propertyId` | number |  |
| `attributes.region` | string |  |
| `attributes.streetAddress` | string |  |
| `attributes.subpremise` | object |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET buildings/:BUILDING_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-building.md) for the provider-specific parameters and requirements.

