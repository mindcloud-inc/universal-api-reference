# Formstack Documents: Convert File to PDF

Converts a file to PDF in Formstack Documents.

```
POST https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/convert-file-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/convert-file-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/convert-file-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file.contents` | string | no | Base64-encoded source file contents |
| `file.name` | string | yes | Name of the source file to convert |
| `file.url` | string | no | Remote URL for the source file |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Formstack Documents API returns.

## Native endpoint

Through the native Formstack Documents API, this operation is `POST /tools/convert_to_pdf` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-file-to-pdf.md) for the provider-specific parameters and requirements.

