# HR Partner: Add or Update Application



```
PUT https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-application', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native HR Partner API, this operation is `POST /application` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-update-application.md) for the provider-specific parameters and requirements.

