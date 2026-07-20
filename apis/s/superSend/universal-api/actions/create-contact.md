# SuperSend: Create Contact

Creates a new contact in SuperSend.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no |  |
| `linkedinUrl` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `company` | string | no |  |
| `title` | string | no |  |
| `phone` | string | no |  |
| `website` | string | no |  |
| `twitter` | string | no |  |
| `custom` | object | no |  |
| `teamId` | string | yes |  |
| `campaignId` | string | yes |  |
| `validateEmails` | boolean | no | When true, runs email verification on the contact (consumes credits). Default is false to avoid surprise billing. Only applies when creating a new contact with an email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_id": "string",
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom": {},
      "deleted": true,
      "email": "ava@example.com",
      "finished": true,
      "first_name": "Ava",
      "id": "string",
      "interest": "string",
      "last_name": "Chen",
      "linkedin_url": "https://example.com",
      "phone": "string",
      "team_id": "string",
      "title": "string",
      "twitter": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | string |  |
| `company` | string |  |
| `created_at` | date |  |
| `custom` | object |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `finished` | boolean |  |
| `first_name` | string |  |
| `id` | string |  |
| `interest` | string |  |
| `last_name` | string |  |
| `linkedin_url` | string |  |
| `phone` | string |  |
| `team_id` | string |  |
| `title` | string |  |
| `twitter` | string |  |
| `updated_at` | date |  |
| `website` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /contacts` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

