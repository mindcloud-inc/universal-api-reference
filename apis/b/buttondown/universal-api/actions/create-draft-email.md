# Buttondown: Create Draft Email

Creates a draft email in Buttondown.

```
POST https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/create-draft-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/create-draft-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/create-draft-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Draft email subject line. |
| `body` | string | yes | Draft email body content. |
| `description` | string | no | Internal description for the draft email. |
| `slug` | string | no | Optional draft slug. |
| `canonical_url` | string | no | Canonical URL for the email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absoluteUrl": "https://example.com",
      "analytics": {},
      "attachments": [
        {}
      ],
      "body": "string",
      "canonicalUrl": "https://example.com",
      "commentingMode": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "emailType": "ava@example.com",
      "featured": true,
      "filters": {},
      "id": "string",
      "image": "string",
      "metadata": {},
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "publishDate": "2026-05-07T12:00:00.000Z",
      "relatedEmailIds": [
        "ava@example.com"
      ],
      "reviewMode": "string",
      "secondaryId": 1,
      "shouldTriggerPayPerEmailBilling": true,
      "slug": "string",
      "source": "string",
      "status": "string",
      "subject": "string",
      "suppressionReason": "string",
      "template": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absoluteUrl` | string | Resolved absolute URL for the email. |
| `analytics` | object | Analytics payload when Buttondown provides one. |
| `attachments` | array<object> | Attachments associated with the email. |
| `body` | string | Email body content returned by Buttondown. |
| `canonicalUrl` | string | Canonical URL associated with the email. |
| `commentingMode` | string | Current commenting mode. |
| `creationDate` | date | When the email was created in Buttondown. |
| `description` | string | Internal description stored on the email. |
| `emailType` | string | Buttondown email type. |
| `featured` | boolean | Whether the email is featured. |
| `filters` | object | Audience filter definition stored on the email. |
| `id` | string | Buttondown email ID. |
| `image` | string | Hero image associated with the email. |
| `metadata` | object | Structured metadata stored on the email. |
| `modificationDate` | date | When the email was last modified in Buttondown. |
| `publishDate` | date | When the email is scheduled or published, if applicable. |
| `relatedEmailIds` | array<string> | Related email IDs returned by Buttondown. |
| `reviewMode` | string | Current review mode. |
| `secondaryId` | number | Secondary numeric ID when Buttondown returns one. |
| `shouldTriggerPayPerEmailBilling` | boolean | Whether the email should trigger pay-per-email billing. |
| `slug` | string | Email slug. |
| `source` | string | How the email was created. |
| `status` | string | Current Buttondown email status. |
| `subject` | string | Email subject line. |
| `suppressionReason` | string | Suppression reason when Buttondown returns one. |
| `template` | object | Template metadata when Buttondown returns one. |

## Native endpoint

Through the native Buttondown API, this operation is `POST /emails` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-email.md) for the provider-specific parameters and requirements.

