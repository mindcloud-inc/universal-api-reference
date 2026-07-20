# Mifiel: Download ZIP File

Retrieves a signed document ZIP archive from Mifiel.

```
GET https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/download-zip-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mifiel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/download-zip-file?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/download-zip-file?${params}`, {
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
| `id` | string | yes | Document ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mifiel API returns.

## Native endpoint

Through the native Mifiel API, this operation is `GET /api/v1/documents/:id/zip` (base URL `https://app.mifiel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-zip-file.md) for the provider-specific parameters and requirements.

