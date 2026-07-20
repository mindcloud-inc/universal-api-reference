# SafetyCulture: Create Issue

Creates a new issue in SafetyCulture.

```
POST https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "categoryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "categoryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | no | Optional. The unique identifier of the incident If not provided, UUID will be generated server side |
| `title` | string | yes | Required. Title of the incident Title is limited to only 255 characters max |
| `createdAt` | date | no | Optional. Date and time this incident was created |
| `categoryId` | string | yes | Required. ID of the incident's category If not set, this incident will be stored with the default category(None) |
| `answeredQuestions[]` | array<string> | no | Optional. An array of all, if any, custom questions that have been answered by the contributor @deprecated: Use `QuestionAnswer` instead. This was a field used for string custom questions. We've since moved to structured custom questions in the `QuestionAnswer` field. |
| `email` | string | no | Optional. The email address of the contributor |
| `media[]` | array<object> | no | Optional. Array of media items to be linked to the incident. |
| `siteId` | string | no | Optional. ID of the site to associate with the incident. If not provided, no site will be associated with the incident. |
| `name` | string | no | Optional. The name of the contributor |
| `contact` | string | no | Optional. The contact details of the contributor |
| `location` | object | no | The location that the incident occurred at |
| `accessToken` | string | no | Optional. The access token used to authenticate the request. This field should be set when following the contributor flow. Otherwise, authenticate via normal means. |
| `description` | string | no | Optional. Description of the issue (maximum 500 characters). |
| `questionsAndAnswers[]` | array<object> | no | Optional. An array of all, if any, custom questions that have been answered for this issue. |
| `items[]` | array<object> | no | Optional. The category fields and questions that applied to this incident when it was created. |
| `occurredAt` | date | no | Optional. Date and time this incident occurred at |
| `assetId` | string | no | Optional. The ID of the asset associated with this incident. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "incidentId": "string",
      "uniqueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `incidentId` | string |  |
| `uniqueId` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `POST /tasks/v1/incidents/submit` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

