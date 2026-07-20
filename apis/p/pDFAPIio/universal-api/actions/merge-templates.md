# PDF-API.io: Merge Templates

Creates one PDF document from multiple templates in PDF-API.io.

```
POST https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/merge-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-API.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/merge-templates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templates[]": [
    {}
  ],
  "templates[].id": 1,
  "templates[].data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/merge-templates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templates[]": [{}],
    "templates[].id": 1,
    "templates[].data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templates[]` | array<object> | yes | The ordered list of templates to merge into a single PDF. |
| `templates[].id` | list<number> | yes | The identifier of the template to merge. |
| `templates[].data` | object | yes | Key-value pairs representing the data to replace in that template before merging. |
| `output` | list<string> | no | Optional output format for the merged PDF response. One of: `pdf`, `url`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | The HTTP-style status returned by PDF-API.io for the merged PDF request. |
| `url` | string | The temporary download URL for the merged PDF when output=url is used. |

## Native endpoint

Through the native PDF-API.io API, this operation is `POST /templates/merge` (base URL `https://pdf-api.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-templates.md) for the provider-specific parameters and requirements.

