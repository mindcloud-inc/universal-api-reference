# Testlify: Get Assessment

Retrieves a specific assessment from Testlify by ID.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-assessment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-assessment?connectionId=$CONNECTION_ID&assessmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assessmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-assessment?${params}`, {
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
| `assessmentId` | string | yes | Assessment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentId": "string",
      "assessmentStatus": "string",
      "assessmentTitle": "string",
      "defaultLanguage": "string",
      "isArchived": true,
      "jobRoleId": "string",
      "name": "Ava Chen",
      "numberOfAttempts": 1,
      "orgId": "string",
      "recipientForNotification": [
        "string"
      ],
      "supportedLanguages": [
        "string"
      ],
      "totalCandidateCount": 1,
      "totalTestLibrary": 1,
      "totalTime": 1,
      "userId": "string",
      "workspaceUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentId` | string |  |
| `assessmentStatus` | string |  |
| `assessmentTitle` | string |  |
| `defaultLanguage` | string |  |
| `isArchived` | boolean |  |
| `jobRoleId` | string |  |
| `name` | string |  |
| `numberOfAttempts` | number |  |
| `orgId` | string |  |
| `recipientForNotification` | array<string> |  |
| `supportedLanguages` | array<string> |  |
| `totalCandidateCount` | number |  |
| `totalTestLibrary` | number |  |
| `totalTime` | number |  |
| `userId` | string |  |
| `workspaceUrl` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/assessment/:assessmentId` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-assessment.md) for the provider-specific parameters and requirements.

