# Bulldog-WP: Preview image

Retrieves an image preview from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/preview-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/preview-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/preview-file?${params}`, {
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
| `fileId` | string | yes | Uploaded file resource ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bulldog-WP API returns.

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /files/{fileId}/preview` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-file.md) for the provider-specific parameters and requirements.

