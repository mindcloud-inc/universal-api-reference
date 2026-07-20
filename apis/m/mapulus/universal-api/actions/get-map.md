# Mapulus: Get Map

Retrieves a specific map from Mapulus.

```
GET https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/get-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mapulus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/get-map?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/get-map?${params}`, {
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
| `id` | string | yes | Map ID. |
| `expand[]` | array<string> | no | Expand related resources such as layers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "object": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the map was created. |
| `id` | string | The map identifier. |
| `object` | string | The resource type returned by Mapulus. |
| `title` | string | The map title. |
| `updatedAt` | date | When the map was last updated. |

## Native endpoint

Through the native Mapulus API, this operation is `GET /api/v1/maps/:id` (base URL `https://api.mapulus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-map.md) for the provider-specific parameters and requirements.

