# Shuffler: Get File Metadata

Retrieves file metadata from Shuffler.

```
GET https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-file-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-file-metadata?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-file-metadata?${params}`, {
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
| `fileId` | string | yes | File Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "id": "string",
      "namespace": "Ava Chen",
      "orgId": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `id` | string |  |
| `namespace` | string |  |
| `orgId` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Shuffler API, this operation is `POST /files/{fileId}` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-metadata.md) for the provider-specific parameters and requirements.

