# Raven Tools: Delete Links

Deletes existing links from Raven Tools.

```
DELETE https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/delete-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/delete-links?connectionId=$CONNECTION_ID&link=JSON%20array%20of%20Raven%20link%20id%20objects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "link": "JSON array of Raven link id objects"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/delete-links?${params}`, {
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
| `domain` | string | no | Optional domain if omitted from each link record. Example: `mindcloud.co`. |
| `link` | string | yes | JSON-encoded string representing one or more Raven link ids to delete. Default: `[{"link id":"31311497"}]`. Example: `JSON array of Raven link id objects`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Raven Tools API returns.

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-links.md) for the provider-specific parameters and requirements.

