# Dropbox Sign: List Signature Requests

Retrieves signature requests from Dropbox Sign.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/list-signature-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/list-signature-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/list-signature-requests?${params}`, {
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
| `accountId` | string | no | Which account to return SignatureRequests for. Use all for all team members. |
| `query` | string | no | Search terms used to filter signature requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {
          "apiId": "string",
          "editor": {},
          "name": "Ava Chen",
          "required": true,
          "type": "string",
          "value": "string"
        }
      ],
      "detailsUrl": "https://example.com",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "filesUrl": "https://example.com",
      "finalCopyUri": "string",
      "hasError": true,
      "isComplete": true,
      "isDeclined": true,
      "message": "string",
      "originalTitle": "string",
      "requesterEmailAddress": "ava@example.com",
      "signatureRequestId": "string",
      "signatures": [
        {
          "error": {},
          "hasPin": true,
          "hasSmsAuth": true,
          "hasSmsDelivery": true,
          "lastRemindedAt": "2026-05-07T12:00:00.000Z",
          "lastViewedAt": "2026-05-07T12:00:00.000Z",
          "order": {},
          "signatureId": "string",
          "signedAt": "2026-05-07T12:00:00.000Z",
          "signerEmailAddress": "ava@example.com",
          "signerName": "Ava Chen",
          "signerRole": {},
          "smsPhoneNumber": {},
          "statusCode": "string"
        }
      ],
      "signerExperience": {
        "formView": "string"
      },
      "signingRedirectUrl": {},
      "signingUrl": "https://example.com",
      "subject": "string",
      "templateIds": {},
      "testMode": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customFields[].apiId` | string |  |
| `customFields[].editor` | object |  |
| `customFields[].name` | string |  |
| `customFields[].required` | boolean |  |
| `customFields[].type` | string |  |
| `customFields[].value` | string |  |
| `detailsUrl` | string |  |
| `expiresAt` | date |  |
| `filesUrl` | string |  |
| `finalCopyUri` | string |  |
| `hasError` | boolean |  |
| `isComplete` | boolean |  |
| `isDeclined` | boolean |  |
| `message` | string |  |
| `originalTitle` | string |  |
| `requesterEmailAddress` | string |  |
| `signatureRequestId` | string |  |
| `signatures[].error` | object |  |
| `signatures[].hasPin` | boolean |  |
| `signatures[].hasSmsAuth` | boolean |  |
| `signatures[].hasSmsDelivery` | boolean |  |
| `signatures[].lastRemindedAt` | date |  |
| `signatures[].lastViewedAt` | date |  |
| `signatures[].order` | object |  |
| `signatures[].signatureId` | string |  |
| `signatures[].signedAt` | date |  |
| `signatures[].signerEmailAddress` | string |  |
| `signatures[].signerName` | string |  |
| `signatures[].signerRole` | object |  |
| `signatures[].smsPhoneNumber` | object |  |
| `signatures[].statusCode` | string |  |
| `signerExperience.formView` | string |  |
| `signingRedirectUrl` | object |  |
| `signingUrl` | string |  |
| `subject` | string |  |
| `templateIds` | object |  |
| `testMode` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Dropbox Sign API, this operation is `GET /signature_request/list` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-requests.md) for the provider-specific parameters and requirements.

