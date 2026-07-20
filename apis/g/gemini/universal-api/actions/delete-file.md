# Gemini: Delete File

Deletes a file from Gemini.

```
DELETE https://connect.mindcloud.co/v1/universal/gemini/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/delete-file?connectionId=$CONNECTION_ID&fileId=gmrlbfnyrvyh" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "gmrlbfnyrvyh"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gemini/latest/actions/delete-file?${params}`, {
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
| `fileId` | string | yes | File ID segment (without `files/` prefix). Example: `gmrlbfnyrvyh`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Empty object returned by Gemini when a file is deleted successfully. |

## Native endpoint

Through the native Gemini API, this operation is `DELETE v1beta/files/:fileId` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

