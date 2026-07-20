# Recruitee ATS: Upload Attachment



```
POST https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/upload-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/upload-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attachment.remote_file_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/upload-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attachment.remote_file_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachment.remote_file_url` | string | yes | Public URL to the attachment file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachment.candidate_id` | number | no | Candidate ID that should receive the attachment. |
| `attachment.offer_id` | number | no | Offer ID that should receive the attachment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachment": {
        "adminId": 1,
        "candidateId": 1,
        "createdAt": "string",
        "extension": "string",
        "filename": "Ava Chen",
        "fileSize": 1,
        "fileUrl": "https://example.com",
        "guestId": {},
        "id": 1,
        "kind": "string",
        "offerId": {},
        "pdfThumbnailUrl": "https://example.com",
        "pdfUrl": "https://example.com",
        "requisitionId": {},
        "source": "string",
        "status": "string",
        "talentPoolId": {},
        "uploader": "string",
        "visibility": {
          "level": "string"
        }
      },
      "references": [
        {
          "adminappUrl": "https://example.com",
          "adminId": 1,
          "createdAt": "string",
          "emails": [
            "ava@example.com"
          ],
          "example": true,
          "hasAvatar": true,
          "id": 1,
          "initials": "string",
          "isAnonymous": true,
          "isHired": true,
          "isRevealed": true,
          "lastMessageAt": {},
          "name": "Ava Chen",
          "pendingResultRequest": true,
          "phones": [
            "string"
          ],
          "photoThumbUrl": "https://example.com",
          "positiveRatings": {},
          "ratingsCount": 1,
          "referrer": {},
          "salutation": {},
          "source": "string",
          "tasksCount": 1,
          "title": {},
          "type": "string",
          "upcomingEvent": true,
          "updatedAt": "string",
          "viewed": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachment.adminId` | number |  |
| `attachment.candidateId` | number |  |
| `attachment.createdAt` | string |  |
| `attachment.extension` | string |  |
| `attachment.filename` | string |  |
| `attachment.fileSize` | number |  |
| `attachment.fileUrl` | string |  |
| `attachment.guestId` | object |  |
| `attachment.id` | number |  |
| `attachment.kind` | string |  |
| `attachment.offerId` | object |  |
| `attachment.pdfThumbnailUrl` | string |  |
| `attachment.pdfUrl` | string |  |
| `attachment.requisitionId` | object |  |
| `attachment.source` | string |  |
| `attachment.status` | string |  |
| `attachment.talentPoolId` | object |  |
| `attachment.uploader` | string |  |
| `attachment.visibility.level` | string |  |
| `references[].adminappUrl` | string |  |
| `references[].adminId` | number |  |
| `references[].createdAt` | string |  |
| `references[].emails[]` | string |  |
| `references[].example` | boolean |  |
| `references[].hasAvatar` | boolean |  |
| `references[].id` | number |  |
| `references[].initials` | string |  |
| `references[].isAnonymous` | boolean |  |
| `references[].isHired` | boolean |  |
| `references[].isRevealed` | boolean |  |
| `references[].lastMessageAt` | object |  |
| `references[].name` | string |  |
| `references[].pendingResultRequest` | boolean |  |
| `references[].phones[]` | string |  |
| `references[].photoThumbUrl` | string |  |
| `references[].positiveRatings` | object |  |
| `references[].ratingsCount` | number |  |
| `references[].referrer` | object |  |
| `references[].salutation` | object |  |
| `references[].source` | string |  |
| `references[].tasksCount` | number |  |
| `references[].title` | object |  |
| `references[].type` | string |  |
| `references[].upcomingEvent` | boolean |  |
| `references[].updatedAt` | string |  |
| `references[].viewed` | boolean |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `POST /c/:company_id/attachments` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment.md) for the provider-specific parameters and requirements.

