# Felt: Export Map Comments

Retrieves exported map comments from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/export-map-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/export-map-comments?connectionId=$CONNECTION_ID&mapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/export-map-comments?${params}`, {
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
| `mapId` | string | yes | The ID of the map to export comments from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list | no | The export format for the comments. One of: `0`, `1`, `2`. Default: `json`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Felt API returns.

## Native endpoint

Through the native Felt API, this operation is `GET /maps/:mapId/comments/export` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-map-comments.md) for the provider-specific parameters and requirements.

