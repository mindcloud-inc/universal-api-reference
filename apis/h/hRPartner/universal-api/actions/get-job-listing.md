# HR Partner: Get Job Listing



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-job-listing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-job-listing?connectionId=$CONNECTION_ID&jobID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-job-listing?${params}`, {
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
      "customForm": {},
      "department": "string",
      "employmentStatus": "string",
      "id": "string",
      "isActive": true,
      "location": "string",
      "position": "string",
      "publishAt": "2026-05-07T12:00:00.000Z",
      "responseEmail": "ava@example.com",
      "scorecard": {},
      "selectionPanel": [
        {}
      ],
      "stages": {},
      "summary": "string",
      "title": "string",
      "unpublishAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customForm` | object |  |
| `department` | string |  |
| `employmentStatus` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `location` | string |  |
| `position` | string |  |
| `publishAt` | date |  |
| `responseEmail` | string |  |
| `scorecard` | object |  |
| `selectionPanel` | array<object> |  |
| `stages` | object |  |
| `summary` | string |  |
| `title` | string |  |
| `unpublishAt` | date |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /job/:jobID` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-listing.md) for the provider-specific parameters and requirements.

