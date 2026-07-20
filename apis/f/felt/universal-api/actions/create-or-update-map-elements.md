# Felt: Create Or Update Map Elements

Creates or updates map elements in Felt.

```
PUT https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-or-update-map-elements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-or-update-map-elements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "features[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-or-update-map-elements', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "features[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The ID of the map to create the elements in. |
| `features[]` | array<object> | yes | GeoJSON features to create or update. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | array<object> | GeoJSON features returned by Felt. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/elements` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-map-elements.md) for the provider-specific parameters and requirements.

