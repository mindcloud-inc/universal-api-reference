# Raven Tools: Delete Link

Deletes an existing link from Raven Tools.

```
DELETE https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/delete-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/delete-link?connectionId=$CONNECTION_ID&link=JSON%20array%20with%20Raven%20link%20ids%20to%20delete." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "link": "JSON array with Raven link ids to delete."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/delete-link?${params}`, {
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
| `link` | string | yes | Default: `[{"link id":"31311496"}]`. Example: `JSON array with Raven link ids to delete.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Raven Tools API returns.

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-link.md) for the provider-specific parameters and requirements.

