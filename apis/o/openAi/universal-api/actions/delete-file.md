# Open AI: Delete File

Deletes a file from Open AI.

```
DELETE https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-file?connectionId=$CONNECTION_ID&file_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/delete-file?${params}`, {
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
| `file_id` | string | yes | OpenAI file ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the file was deleted. |
| `id` | string | Deleted file ID. |
| `object` | string | Object type. |

## Native endpoint

Through the native Open AI API, this operation is `DELETE v1/files/:file_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

