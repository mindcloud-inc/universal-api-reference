# Amazon Seller: Get FBM Report Document

Retrieves FBM report document details from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fbm-report-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fbm-report-document?connectionId=$CONNECTION_ID&reportDocumentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportDocumentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fbm-report-document?${params}`, {
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
| `reportDocumentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compressionAlgorithm": "string",
      "reportDocumentId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compressionAlgorithm` | string |  |
| `reportDocumentId` | string |  |
| `url` | string | A presigned URL for the report document. This URL expires after 5 minutes. |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET reports/2021-06-30/documents/:reportDocumentId` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fbm-report-document.md) for the provider-specific parameters and requirements.

