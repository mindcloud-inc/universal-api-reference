# LessonBuddy: Create Lead

Creates a new lead in LessonBuddy.

```
POST https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locationId": 1,
  "firstName": "Ava",
  "lastName": "Chen",
  "emailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locationId": 1,
    "firstName": "Ava",
    "lastName": "Chen",
    "emailAddress": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | number | yes | LessonBuddy location ID for the lead. |
| `firstName` | string | yes | Lead first name. At least one of first name or last name is required by LessonBuddy. |
| `lastName` | string | yes | Lead last name. At least one of first name or last name is required by LessonBuddy. |
| `emailAddress` | string | yes | Lead email address. At least one contact method, email or cell phone, is required by LessonBuddy. |
| `cellPhone` | string | no | Lead cell phone. At least one contact method, email or cell phone, is required by LessonBuddy. |
| `marketingOptIn` | boolean | no | Whether the customer consented to marketing opt-in. Default: `false`. |
| `tags[].tag` | string | no | Lead tag. LessonBuddy recommends complete-lead-form. Default: `complete-lead-form`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "clientPlatformId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdById": 1,
      "familyId": 1,
      "id": 1,
      "locationId": 1,
      "meta": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedById": 1,
      "utmCodeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `clientPlatformId` | string |  |
| `createdAt` | date |  |
| `createdById` | number |  |
| `familyId` | number |  |
| `id` | number |  |
| `locationId` | number |  |
| `meta` | object |  |
| `updatedAt` | date |  |
| `updatedById` | number |  |
| `utmCodeId` | number |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `POST /v2/campaign/leads` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

