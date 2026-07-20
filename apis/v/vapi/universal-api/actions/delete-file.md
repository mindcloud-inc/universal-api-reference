# Vapi: Delete File

Deletes an existing file from Vapi.

```
DELETE https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-file?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-file?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket": "string",
      "bytes": 1,
      "createdAt": "string",
      "id": "string",
      "key": "string",
      "metadata": {},
      "mimetype": "string",
      "name": "Ava Chen",
      "object": "string",
      "orgId": "string",
      "originalName": "Ava Chen",
      "parsedTextBytes": 1,
      "parsedTextUrl": "https://example.com",
      "path": "string",
      "purpose": "string",
      "status": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket` | string |  |
| `bytes` | number |  |
| `createdAt` | string | This is the ISO 8601 date-time string of when the file was created. |
| `id` | string | This is the unique identifier for the file. |
| `key` | string |  |
| `metadata` | object |  |
| `mimetype` | string |  |
| `name` | string | This is the name of the file. This is just for your own reference. |
| `object` | string |  |
| `orgId` | string | This is the unique identifier for the org that this file belongs to. |
| `originalName` | string |  |
| `parsedTextBytes` | number |  |
| `parsedTextUrl` | string |  |
| `path` | string |  |
| `purpose` | string |  |
| `status` | string |  |
| `updatedAt` | string | This is the ISO 8601 date-time string of when the file was last updated. |
| `url` | string |  |

## Native endpoint

Through the native Vapi API, this operation is `DELETE /file/:id` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

