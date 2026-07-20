# Testlify: Create Compose Assessment

Creates a custom assessment in Testlify from scratch.

```
POST https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-compose-assessment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-compose-assessment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "testLibraryIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-compose-assessment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "testLibraryIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `testLibraryIds[]` | array<string> | yes |  |
| `settings.extraTime` | number | no |  |
| `settings.feedbackRating` | number | no |  |
| `settings.feedbackRemark` | string | no |  |
| `settings.verifyPassword` | string | no |  |
| `settings.welcomeVideoUploadUrl` | string | no |  |
| `settings.welcomeVideoKey` | string | no |  |
| `settings.welcomeVideoPath` | string | no |  |
| `settings.externalWelcomeVideoLink` | string | no |  |
| `settings.autoPlayWelcomeVideo` | boolean | no |  |
| `settings.titleSlug` | string | no |  |
| `settings.attemptTestLibrariesRequired` | boolean | no |  |
| `settings.webcamAndMicrophoneAccessRequired` | boolean | no |  |
| `settings.snapshotCaptureRequired` | boolean | no |  |
| `settings.snapshotIntervalType` | string | no |  |
| `settings.customSnapshotInterval` | number | no |  |
| `settings.defaultLanguage` | string | no |  |
| `settings.supportedLanguages[]` | array<string> | no |  |
| `settings.skipRegistration` | boolean | no |  |
| `settings.enableFeedbackAfterSection` | boolean | no |  |
| `settings.enableFeedback` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentStatus": "string",
      "created": "string",
      "defaultLanguage": "string",
      "id": "string",
      "isArchived": true,
      "jobRoleId": "string",
      "language": "string",
      "lastModifiedBy": "string",
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
      "testAdministratorNotification": "string",
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
| `assessmentStatus` | string |  |
| `created` | string |  |
| `defaultLanguage` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `jobRoleId` | string |  |
| `language` | string |  |
| `lastModifiedBy` | string |  |
| `modified` | string |  |
| `numberOfAttempts` | number |  |
| `orgId` | string |  |
| `otherJobRole` | string |  |
| `recipientForNotification` | array<string> |  |
| `supportedLanguages` | array<string> |  |
| `testAdministratorNotification` | string |  |
| `title` | string |  |
| `titleSlug` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `POST /v1/assessment/compose` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-compose-assessment.md) for the provider-specific parameters and requirements.

