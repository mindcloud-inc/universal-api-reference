# RUIAN: Get service details

Retrieves service details from RUIAN API.

```
GET https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-service-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RUIAN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-service-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-service-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilities": "string",
      "cimVersion": "string",
      "copyrightText": "string",
      "currentVersion": 1,
      "description": "string",
      "exportTilesAllowed": true,
      "layers": [
        {}
      ],
      "mapName": "Ava Chen",
      "maxRecordCount": 1,
      "serviceDescription": "string",
      "spatialReference": {},
      "supportedImageFormatTypes": "string",
      "supportedQueryFormats": "string",
      "supportsDynamicLayers": true,
      "tables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities` | string |  |
| `cimVersion` | string |  |
| `copyrightText` | string |  |
| `currentVersion` | number |  |
| `description` | string |  |
| `exportTilesAllowed` | boolean |  |
| `layers` | array<object> |  |
| `mapName` | string |  |
| `maxRecordCount` | number |  |
| `serviceDescription` | string |  |
| `spatialReference` | object |  |
| `supportedImageFormatTypes` | string |  |
| `supportedQueryFormats` | string |  |
| `supportsDynamicLayers` | boolean |  |
| `tables` | array<object> |  |

## Native endpoint

Through the native RUIAN API, this operation is `GET /` (base URL `https://ags.cuzk.gov.cz/arcgis/rest/services/RUIAN/MapServer`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-details.md) for the provider-specific parameters and requirements.

