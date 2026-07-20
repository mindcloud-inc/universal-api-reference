# Dify: Delete Annotation

Deletes an existing annotation from Dify.

```
DELETE https://connect.mindcloud.co/v1/universal/dify/latest/actions/delete-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dify/latest/actions/delete-annotation?connectionId=$CONNECTION_ID&annotationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "annotationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/delete-annotation?${params}`, {
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
| `annotationId` | string | yes | Annotation ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dify API returns.

## Native endpoint

Through the native Dify API, this operation is `DELETE /apps/annotations/:annotation_id` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-annotation.md) for the provider-specific parameters and requirements.

