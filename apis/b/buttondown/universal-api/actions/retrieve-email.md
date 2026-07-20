# Buttondown: Retrieve Email

Retrieves an email from Buttondown.

```
GET https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-email?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-email?${params}`, {
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
| `id` | string | yes | Email ID. |

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

Through the native Buttondown API, this operation is `GET /emails/:id` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-email.md) for the provider-specific parameters and requirements.

