# Uploadcare: Copy File To Local Storage

Creates a local storage copy in Uploadcare.

```
POST https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/copy-file-to-local-storage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/copy-file-to-local-storage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/copy-file-to-local-storage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Metadata object to attach to the copied file. |
| `source` | string | yes | Source file UUID or URL to copy into local storage. |
| `store` | string | no | Whether to store the copied file permanently. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Copied file record returned by Uploadcare. |
| `type` | string | Uploadcare copy result type. |

## Native endpoint

Through the native Uploadcare API, this operation is `POST /files/local_copy/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-file-to-local-storage.md) for the provider-specific parameters and requirements.

