# Felt: Get Map

Retrieves a map from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map?connectionId=$CONNECTION_ID&mapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map?${params}`, {
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
| `mapId` | string | yes | Map ID to retrieve. |

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

Through the native Felt API, this operation is `GET /maps/:mapId` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-map.md) for the provider-specific parameters and requirements.

