# Felt: Create Map

Creates a new map in Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-map" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-map', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Map title. |
| `publicAccess` | string | no | Map sharing level. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Map description shown in the legend. |
| `basemap` | string | no | Basemap name or tile URL. |
| `lat` | number | no | Initial map latitude. |
| `lon` | number | no | Initial map longitude. |
| `zoom` | number | no | Initial map zoom level. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "basemap": "string",
      "elements": {},
      "id": "string",
      "layer_groups": [
        {}
      ],
      "layers": [
        {}
      ],
      "project_id": "string",
      "public_access": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `basemap` | string | Basemap value. |
| `elements` | object | Annotation feature collection. |
| `id` | string | Felt map ID. |
| `layer_groups` | array<object> | Layer groups on the map. |
| `layers` | array<object> | Layers on the map. |
| `project_id` | string | Parent project ID. |
| `public_access` | string | Map access level. |
| `title` | string | Map title. |
| `type` | string | Returned resource type. |
| `url` | string | Felt map URL. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-map.md) for the provider-specific parameters and requirements.

