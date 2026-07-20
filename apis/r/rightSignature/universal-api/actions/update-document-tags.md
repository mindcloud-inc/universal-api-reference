# RightSignature: Update Document Tags

Replaces tags on an existing RightSignature document.

```
POST https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/update-document-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/update-document-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tags": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/update-document-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tags": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags` | string | yes | Key value tags for categorization |
| `id` | string | yes | Id value |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audits": [
        "string"
      ],
      "currentSignerId": "string",
      "embedCodes": "string",
      "executedAt": "string",
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "id": "string",
      "identityMethod": "string",
      "inPerson": true,
      "mergeFieldValues": [
        "string"
      ],
      "name": "Ava Chen",
      "originalFileUrl": "https://example.com",
      "pageImageUrls": [
        "https://example.com"
      ],
      "passcodePinEnabled": true,
      "recipients": [
        {}
      ],
      "sender": {},
      "sentAt": "2026-05-07T12:00:00.000Z",
      "sharedWith": [
        "string"
      ],
      "signedPdfUrl": "https://example.com",
      "state": "string",
      "tags": {},
      "thumbnailUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audits` | array<string> |  |
| `currentSignerId` | string |  |
| `embedCodes` | string |  |
| `executedAt` | string |  |
| `expiredAt` | date |  |
| `filename` | string |  |
| `id` | string |  |
| `identityMethod` | string |  |
| `inPerson` | boolean |  |
| `mergeFieldValues` | array<string> |  |
| `name` | string |  |
| `originalFileUrl` | string |  |
| `pageImageUrls` | array<string> |  |
| `passcodePinEnabled` | boolean |  |
| `recipients` | array<object> |  |
| `sender` | object |  |
| `sentAt` | date |  |
| `sharedWith` | array<string> |  |
| `signedPdfUrl` | string |  |
| `state` | string |  |
| `tags` | object |  |
| `thumbnailUrl` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `POST /documents/:id/update_tags` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-tags.md) for the provider-specific parameters and requirements.

