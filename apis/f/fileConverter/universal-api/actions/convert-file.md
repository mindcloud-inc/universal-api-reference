# File Converter: Convert File

Convert a file to a specific format

```
GET https://connect.mindcloud.co/v1/universal/fileConverter/latest/actions/convert-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a File Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileConverter/latest/actions/convert-file?connectionId=$CONNECTION_ID&file=string&outputFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string",
  "outputFormat": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileConverter/latest/actions/convert-file?${params}`, {
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
| `file` | file | yes | The file to be converted. |
| `outputFormat` | list | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native File Converter API returns.

## Native endpoint

Through the native File Converter API, this operation is `GET`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-file.md) for the provider-specific parameters and requirements.

