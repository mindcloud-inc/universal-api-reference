# DocuPanda - Document Understanding: Health Check

Retrieves service health details from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/health-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/health-check?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /health` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-check.md) for the provider-specific parameters and requirements.

