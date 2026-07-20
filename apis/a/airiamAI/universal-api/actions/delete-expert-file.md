# Airiam AI: Delete Expert File

Deletes an existing expert file from Airiam AI.

```
DELETE https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/delete-expert-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/delete-expert-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/delete-expert-file?${params}`, {
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
| `fileId` | string | yes | Expert file identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the deletion was successful. |

## Native endpoint

Through the native Airiam AI API, this operation is `DELETE /api/v1/plus/file/:fileId` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-expert-file.md) for the provider-specific parameters and requirements.

