# AITable.ai: Delete Embedded Link

Deletes an existing embedded link from AITable.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-embedded-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-embedded-link?connectionId=$CONNECTION_ID&spaceId=string&nodeId=string&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "nodeId": "string",
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-embedded-link?${params}`, {
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
| `spaceId` | string | yes | AITable space ID containing the node. |
| `nodeId` | string | yes | AITable node ID containing the embedded link. |
| `linkId` | string | yes | Embedded link ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AITable.ai API returns.

## Native endpoint

Through the native AITable.ai API, this operation is `DELETE /fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks/:linkId` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-embedded-link.md) for the provider-specific parameters and requirements.

