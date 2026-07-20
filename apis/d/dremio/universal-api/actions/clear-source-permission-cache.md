# Dremio: Clear Source Permission Cache

Clears a source permission cache in Dremio.

```
DELETE https://connect.mindcloud.co/v1/universal/dremio/latest/actions/clear-source-permission-cache
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/clear-source-permission-cache?connectionId=$CONNECTION_ID&projectId=string&sourceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "sourceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/clear-source-permission-cache?${params}`, {
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
| `projectId` | string | yes |  |
| `sourceName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Dremio API, this operation is `DELETE /projects/:project_id/source/:source_name/permission-cache` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-source-permission-cache.md) for the provider-specific parameters and requirements.

