# SigningHub: Get Document Verification

Retrieves document verification details from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-document-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-document-verification?connectionId=$CONNECTION_ID&documentId=1&packageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "1",
  "packageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-document-verification?${params}`, {
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
| `documentId` | number | yes | The document ID to verify. |
| `packageId` | number | yes | Package ID of the package to which the document belongs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certified": true,
      "error_message": "string",
      "field_name": "Ava Chen",
      "ltv": true,
      "page_number": 1,
      "qualified": true,
      "signature_status": "string",
      "signer_name": "Ava Chen",
      "signing_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certified` | boolean |  |
| `error_message` | string |  |
| `field_name` | string |  |
| `ltv` | boolean |  |
| `page_number` | number |  |
| `qualified` | boolean |  |
| `signature_status` | string |  |
| `signer_name` | string |  |
| `signing_time` | date |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/documents/:documentId/verification` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-verification.md) for the provider-specific parameters and requirements.

