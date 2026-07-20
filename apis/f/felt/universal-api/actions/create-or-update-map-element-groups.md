# Felt: Create Or Update Map Element Groups

Creates or updates map element groups in Felt.

```
PUT https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-or-update-map-element-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-or-update-map-element-groups" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "elementGroups[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-or-update-map-element-groups', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "elementGroups[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The ID of the map to create the group in. |
| `elementGroups[]` | array<object> | yes | Element groups to create or update. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "elements": {},
      "id": "string",
      "name": "Ava Chen",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Element group color. |
| `elements` | object | GeoJSON elements in the group. |
| `id` | string | Element group identifier. |
| `name` | string | Element group name. |
| `symbol` | string | Element group symbol. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/element_groups` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-map-element-groups.md) for the provider-specific parameters and requirements.

