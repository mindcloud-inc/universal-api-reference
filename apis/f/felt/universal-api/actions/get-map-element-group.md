# Felt: Get Map Element Group

Retrieves a map element group from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map-element-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map-element-group?connectionId=$CONNECTION_ID&mapId=string&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string",
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map-element-group?${params}`, {
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
| `mapId` | string | yes | The ID of the map. |
| `groupId` | string | yes | The ID of the element group. |

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
| `features` | array<object> | Elements in the requested group. |
| `type` | string | GeoJSON collection type. |

## Native endpoint

Through the native Felt API, this operation is `GET /maps/:mapId/element_groups/:groupId` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-map-element-group.md) for the provider-specific parameters and requirements.

