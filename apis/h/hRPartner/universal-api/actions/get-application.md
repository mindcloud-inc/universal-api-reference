# HR Partner: Get Application



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-application?connectionId=$CONNECTION_ID&applicationID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-application?${params}`, {
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
| `applicationID` | string | yes | Application ID from HR Partner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicant": {},
      "attachments": [
        {}
      ],
      "comments": [
        {}
      ],
      "customForm": {},
      "id": 1,
      "interviews": [
        {}
      ],
      "isActive": true,
      "isArchived": true,
      "isClosed": true,
      "isFlagged": true,
      "isHired": true,
      "isRead": true,
      "jobListing": {},
      "scorecards": [
        {}
      ],
      "source": "string",
      "stage": {},
      "submittedAt": "2026-05-07T12:00:00.000Z",
      "totalScore": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicant` | object |  |
| `attachments` | array<object> |  |
| `comments` | array<object> |  |
| `customForm` | object |  |
| `id` | number |  |
| `interviews` | array<object> |  |
| `isActive` | boolean |  |
| `isArchived` | boolean |  |
| `isClosed` | boolean |  |
| `isFlagged` | boolean |  |
| `isHired` | boolean |  |
| `isRead` | boolean |  |
| `jobListing` | object |  |
| `scorecards` | array<object> |  |
| `source` | string |  |
| `stage` | object |  |
| `submittedAt` | date |  |
| `totalScore` | number |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /application/:applicationID` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application.md) for the provider-specific parameters and requirements.

