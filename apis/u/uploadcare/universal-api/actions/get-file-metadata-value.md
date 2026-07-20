# Uploadcare: Get File Metadata Value

Retrieves a file metadata value from Uploadcare by key.

```
GET https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-file-metadata-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-file-metadata-value?connectionId=$CONNECTION_ID&key=string&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-file-metadata-value?${params}`, {
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
| `key` | string | yes | Metadata key name. |
| `uuid` | string | yes | Uploadcare file UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Uploadcare API returns.

## Native endpoint

Through the native Uploadcare API, this operation is `GET /files/:uuid/metadata/:key/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-metadata-value.md) for the provider-specific parameters and requirements.

