# RUIAN: Get layer details

Retrieves layer details from RUIAN API.

```
GET https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-layer-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RUIAN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-layer-details?connectionId=$CONNECTION_ID&layerId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "layerId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-layer-details?${params}`, {
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
| `layerId` | number | yes | Numeric RUIAN layer ID, for example 0 for ParcelaDefinicniBod. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayField": "string",
      "fields": [
        {}
      ],
      "geometryType": "string",
      "id": 1,
      "maxRecordCount": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `displayField` | string |  |
| `fields` | array<object> |  |
| `geometryType` | string |  |
| `id` | number |  |
| `maxRecordCount` | number |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native RUIAN API, this operation is `GET /{layerId}` (base URL `https://ags.cuzk.gov.cz/arcgis/rest/services/RUIAN/MapServer`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-layer-details.md) for the provider-specific parameters and requirements.

