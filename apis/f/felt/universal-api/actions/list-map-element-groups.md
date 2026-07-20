# Felt: List Map Element Groups

Retrieves map element groups from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-element-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-element-groups?connectionId=$CONNECTION_ID&mapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-element-groups?${params}`, {
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
| `mapId` | string | yes | The ID of the map to list groups from. |

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

Through the native Felt API, this operation is `GET /maps/:mapId/element_groups` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-map-element-groups.md) for the provider-specific parameters and requirements.

