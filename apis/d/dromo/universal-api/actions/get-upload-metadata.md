# Dromo: Get Upload Metadata

Retrieves metadata for an upload from Dromo.

```
GET https://connect.mindcloud.co/v1/universal/dromo/latest/actions/get-upload-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dromo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/get-upload-metadata?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dromo/latest/actions/get-upload-metadata?${params}`, {
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
| `id` | string | yes | Path parameter id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dromo API returns.

## Native endpoint

Through the native Dromo API, this operation is `GET /upload/:id/metadata/` (base URL `https://app.dromo.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-metadata.md) for the provider-specific parameters and requirements.

