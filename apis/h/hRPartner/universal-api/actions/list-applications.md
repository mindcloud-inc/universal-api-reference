# HR Partner: List Applications



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-applications?connectionId=$CONNECTION_ID&jobID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-applications?${params}`, {
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
| `jobID` | string | yes | Job listing ID from HR Partner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicantId": "string",
      "customForm": {},
      "email": "ava@example.com",
      "firstNames": "Ava",
      "id": 1,
      "isArchived": true,
      "isFlagged": true,
      "isHired": true,
      "isRead": true,
      "jobId": "string",
      "lastName": "Chen",
      "source": "string",
      "stage": "string",
      "submittedAt": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantId` | string |  |
| `customForm` | object |  |
| `email` | string |  |
| `firstNames` | string |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `isFlagged` | boolean |  |
| `isHired` | boolean |  |
| `isRead` | boolean |  |
| `jobId` | string |  |
| `lastName` | string |  |
| `source` | string |  |
| `stage` | string |  |
| `submittedAt` | date |  |
| `title` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /applications/:jobID` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.

