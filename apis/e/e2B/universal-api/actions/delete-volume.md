# E2B: Delete Volume

Deletes a team volume from E2B.

```
DELETE https://connect.mindcloud.co/v1/universal/e2B/latest/actions/delete-volume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/delete-volume?connectionId=$CONNECTION_ID&volumeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "volumeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/delete-volume?${params}`, {
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
| `volumeId` | string | yes | Identifier of the volume. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native E2B API returns.

## Native endpoint

Through the native E2B API, this operation is `DELETE /volumes/{volumeID}` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-volume.md) for the provider-specific parameters and requirements.

