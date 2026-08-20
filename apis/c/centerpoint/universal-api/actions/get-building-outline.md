# Centerpoint: Get Building Outline



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-outline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-outline?connectionId=$CONNECTION_ID&BUILDING_OUTLINES_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BUILDING_OUTLINES_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-outline?${params}`, {
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
| `BUILDING_OUTLINES_ID` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "aerialUrl": "https://example.com",
        "buildingDivisionId": 1,
        "createdAt": "string",
        "customOutline": {
          "center": [
            1
          ],
          "label": [
            {}
          ],
          "paths": [
            {}
          ],
          "zoom": 1
        },
        "deletedAt": {},
        "label": "string",
        "outline": {
          "center": [
            1
          ],
          "label": [
            {}
          ],
          "paths": [
            {}
          ],
          "zoom": 1
        },
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
| `attributes.aerialUrl` | string |  |
| `attributes.buildingDivisionId` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.customOutline.center` | array<number> |  |
| `attributes.customOutline.label` | array<object> |  |
| `attributes.customOutline.paths` | array<object> |  |
| `attributes.customOutline.zoom` | number |  |
| `attributes.deletedAt` | object |  |
| `attributes.label` | string |  |
| `attributes.outline.center` | array<number> |  |
| `attributes.outline.label` | array<object> |  |
| `attributes.outline.paths` | array<object> |  |
| `attributes.outline.zoom` | number |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET building_outlines/:BUILDING_OUTLINES_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-building-outline.md) for the provider-specific parameters and requirements.

