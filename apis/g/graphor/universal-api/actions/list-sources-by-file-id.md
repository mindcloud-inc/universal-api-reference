# Graphor: List Sources By File ID

Finds sources in Graphor by file ID.

```
GET https://connect.mindcloud.co/v1/universal/graphor/latest/actions/list-sources-by-file-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/list-sources-by-file-id?connectionId=$CONNECTION_ID&fileIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphor/latest/actions/list-sources-by-file-id?${params}`, {
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
| `fileIds` | string | yes | Optional list of source file IDs to filter the results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileId": "string",
      "fileName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileId` | string |  |
| `fileName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Graphor API, this operation is `GET /` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sources-by-file-id.md) for the provider-specific parameters and requirements.

