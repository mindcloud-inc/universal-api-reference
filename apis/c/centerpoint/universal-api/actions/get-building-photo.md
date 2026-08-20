# Centerpoint: Get Building Photo



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-photo?connectionId=$CONNECTION_ID&BUILDING_PHOTO_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BUILDING_PHOTO_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-photo?${params}`, {
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
| `BUILDING_PHOTO_ID` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "buildingDivisionId": 1,
        "buildingId": 1,
        "createdAt": "string",
        "deletedAt": {},
        "description": {},
        "imageId": 1,
        "latitude": 1,
        "longitude": 1,
        "name": {},
        "type": "string",
        "updatedAt": "string"
      },
      "id": "string",
      "relationships": {
        "buildingOutline": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "image": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.buildingDivisionId` | number |  |
| `attributes.buildingId` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.description` | object |  |
| `attributes.imageId` | number |  |
| `attributes.latitude` | number |  |
| `attributes.longitude` | number |  |
| `attributes.name` | object |  |
| `attributes.type` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.buildingOutline.data.id` | string |  |
| `relationships.buildingOutline.data.type` | string |  |
| `relationships.image.data.id` | string |  |
| `relationships.image.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET building_photos/:BUILDING_PHOTO_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-building-photo.md) for the provider-specific parameters and requirements.

