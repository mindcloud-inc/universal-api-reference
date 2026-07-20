# SigningHub: Get Document Details

Retrieves document details from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-document-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-document-details?connectionId=$CONNECTION_ID&documentId=1&packageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "1",
  "packageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-document-details?${params}`, {
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
| `documentId` | number | yes | The document ID for which the details are requested. |
| `packageId` | number | yes | The package ID of the package to which the document belongs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certify": {},
      "document_id": 1,
      "document_name": "Ava Chen",
      "document_order": 1,
      "document_pages": 1,
      "document_type": "string",
      "form_fields": true,
      "modified_on": "2026-05-07T12:00:00.000Z",
      "template": {},
      "uploaded_on": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certify` | object |  |
| `document_id` | number |  |
| `document_name` | string |  |
| `document_order` | number |  |
| `document_pages` | number |  |
| `document_type` | string |  |
| `form_fields` | boolean |  |
| `modified_on` | date |  |
| `template` | object |  |
| `uploaded_on` | date |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/documents/:documentId/details` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-details.md) for the provider-specific parameters and requirements.

