# Docmosis: Convert File



```
POST https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/convert-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/convert-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "https://files.catbox.moe/50iz06.xlsx",
  "outputName": "docmosis-convert-output.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/convert-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "https://files.catbox.moe/50iz06.xlsx",
    "outputName": "docmosis-convert-output.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Document file to convert. Example: `https://files.catbox.moe/50iz06.xlsx`. |
| `outputName` | string | yes | Output filename including desired extension, for example output.pdf. Example: `docmosis-convert-output.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Converted document bytes returned by Docmosis. |
| `type` | string | Buffer type marker for the converted binary output. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /convert` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-file.md) for the provider-specific parameters and requirements.

