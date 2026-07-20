# Testlify: Create Assessment From Template

Creates a Testlify assessment from an existing template.

```
POST https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-assessment-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-assessment-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-assessment-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentDescription": "string",
      "assessmentStatus": "string",
      "created": "string",
      "defaultLanguage": "string",
      "id": "string",
      "isArchived": true,
      "jobRoleId": "string",
      "language": "string",
      "modified": "string",
      "numberOfAttempts": 1,
      "orgId": "string",
      "otherJobRole": "string",
      "recipientForNotification": [
        "string"
      ],
      "supportedLanguages": [
        "string"
      ],
      "title": "string",
      "titleSlug": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentDescription` | string |  |
| `assessmentStatus` | string |  |
| `created` | string |  |
| `defaultLanguage` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `jobRoleId` | string |  |
| `language` | string |  |
| `modified` | string |  |
| `numberOfAttempts` | number |  |
| `orgId` | string |  |
| `otherJobRole` | string |  |
| `recipientForNotification` | array<string> |  |
| `supportedLanguages` | array<string> |  |
| `title` | string |  |
| `titleSlug` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `POST /v1/reseller/assessment` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-assessment-from-template.md) for the provider-specific parameters and requirements.

