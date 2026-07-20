# QuestionPro Surveys: Get Organization



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=1234567" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1234567"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-organization?${params}`, {
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
| `organizationId` | number | yes | The QuestionPro organization ID. Example: `1234567`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountRepEmail": "ava@example.com",
      "dashboardUserCount": 1,
      "license": "string",
      "name": "Ava Chen",
      "organizationID": 1,
      "primaryAccountID": 1,
      "primaryAccountUsername": "Ava Chen",
      "shortUrl": "https://example.com",
      "smtpRelay": "string",
      "styleSheet": "string",
      "usage": {},
      "userCount": 1,
      "welcomeHTML": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountRepEmail` | string |  |
| `dashboardUserCount` | number |  |
| `license` | string |  |
| `name` | string |  |
| `organizationID` | number |  |
| `primaryAccountID` | number |  |
| `primaryAccountUsername` | string |  |
| `shortUrl` | string |  |
| `smtpRelay` | string |  |
| `styleSheet` | string |  |
| `usage` | object |  |
| `userCount` | number |  |
| `welcomeHTML` | string |  |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET organizations/:organizationId` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

