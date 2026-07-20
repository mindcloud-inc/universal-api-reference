# Pipedream: Delete a source

Deletes an existing source from Pipedream.

```
DELETE https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/delete-a-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/delete-a-source?connectionId=$CONNECTION_ID&sourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/delete-a-source?${params}`, {
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
| `sourceId` | string | yes | The source identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedream API returns.

## Native endpoint

Through the native Pipedream API, this operation is `DELETE /sources/{id}` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-source.md) for the provider-specific parameters and requirements.

