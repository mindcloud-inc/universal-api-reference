# Weaviate Vector Store: Get backup restoration status

Retrieves backup restoration status from Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/backups-restore-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/backups-restore-status?connectionId=$CONNECTION_ID&backend=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "backend": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/backups-restore-status?${params}`, {
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
| `backend` | string | yes | Specifies the backend storage system where the backup resides (e.g., `filesystem`, `gcs`, `s3`, `azure`). |
| `id` | string | yes | The unique identifier of the backup being restored. Must be URL-safe and compatible with filesystem paths (only lowercase, numbers, underscore, minus characters allowed). |
| `bucket` | string | no | Optional: Specifies the bucket, container, or volume name if required by the backend. |
| `path` | string | no | Optional: Specifies the path within the bucket. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weaviate Vector Store API returns.

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `GET /backups/:backend/:id/restore` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/backups-restore-status.md) for the provider-specific parameters and requirements.

