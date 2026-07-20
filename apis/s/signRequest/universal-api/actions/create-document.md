# SignRequest: Create Document



```
POST https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileFromUrl` | string | no | Publicly accessible URL of the document to download Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `name` | string | no | Defaults to filename, including extension Example: `agreement.pdf`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileFromContent` | string | no | Base64 encoded document content Example: `JVBERi0xLjQKJcTl8uXr...`. |
| `fileFromContentName` | string | no | Filename, including extension, required when using file_from_content Example: `contract.pdf`. |
| `template` | string | no | Template URI to use for the document Example: `https://signrequest.com/api/v1/templates/<uuid>/`. |
| `externalId` | string | no | ID used to reference document in external system Example: `crm-doc-123`. |
| `eventsCallbackUrl` | string | no | URL that should receive document event callbacks Example: `https://example.com/signrequest-events`. |
| `autoDeleteDays` | number | no | Automatically delete finished documents after this many days Example: `30`. |
| `autoExpireDays` | number | no | Automatically expire unfinished documents after this many days Example: `14`. |
| `frontendId` | string | no | Shared secret used with the SignRequest JS client to grant document access Example: `shared-secret-123`. |
| `fileFromSf` | object | no | Salesforce file source configuration |
| `prefillTags[]` | array<object> | no | Prefill signer input data for templates |
| `integrations[]` | array<object> | no | Integration-specific document metadata |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUsed": true,
      "attachments": [
        [
          {}
        ]
      ],
      "autoDeleteAfter": "2026-05-07T12:00:00.000Z",
      "autoDeleteDays": 1,
      "autoExpireAfter": "2026-05-07T12:00:00.000Z",
      "autoExpireDays": 1,
      "eventsCallbackUrl": "https://example.com",
      "externalId": "string",
      "file": "string",
      "fileAsPdf": "string",
      "fileFromSf": {},
      "fileFromUrl": "https://example.com",
      "integrations": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "pdf": "string",
      "prefillTags": [
        [
          {}
        ]
      ],
      "processing": true,
      "sandbox": true,
      "securityHash": "string",
      "shortId": "string",
      "signingLog": {},
      "signrequest": {},
      "status": "string",
      "team": {},
      "template": "string",
      "url": "https://example.com",
      "user": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUsed` | boolean |  |
| `attachments[]` | array<object> |  |
| `autoDeleteAfter` | date |  |
| `autoDeleteDays` | number |  |
| `autoExpireAfter` | date |  |
| `autoExpireDays` | number |  |
| `eventsCallbackUrl` | string |  |
| `externalId` | string |  |
| `file` | string |  |
| `fileAsPdf` | string |  |
| `fileFromSf` | object |  |
| `fileFromUrl` | string |  |
| `integrations[]` | array<object> |  |
| `name` | string |  |
| `pdf` | string |  |
| `prefillTags[]` | array<object> |  |
| `processing` | boolean |  |
| `sandbox` | boolean |  |
| `securityHash` | string |  |
| `shortId` | string |  |
| `signingLog` | object |  |
| `signrequest` | object |  |
| `status` | string |  |
| `team` | object |  |
| `template` | string |  |
| `url` | string |  |
| `user` | object |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.lastName` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `POST /documents/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

