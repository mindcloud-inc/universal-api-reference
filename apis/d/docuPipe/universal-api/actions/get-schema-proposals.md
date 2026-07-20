# DocuPipe: Get Schema Proposals

Retrieves schema proposals for a DocuPipe document.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-schema-proposals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-schema-proposals?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-schema-proposals?${params}`, {
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
| `documentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentDescription": "string",
      "schemas": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentDescription` | string |  |
| `schemas` | array<object> |  |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /document/:documentId/proposed-schemas` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schema-proposals.md) for the provider-specific parameters and requirements.

