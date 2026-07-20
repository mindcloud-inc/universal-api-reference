# HR Partner: Get Application Stage Tracking



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-application-stage-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-application-stage-tracking?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-application-stage-tracking?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "applicantEmail": "ava@example.com",
      "applicantFirstNames": "Ava",
      "applicantFullName": "Ava Chen",
      "applicantId": "string",
      "applicantLastName": "Chen",
      "changedAt": "2026-05-07T12:00:00.000Z",
      "fromStage": "string",
      "id": 1,
      "jobId": "string",
      "jobTitle": "string",
      "toStage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantEmail` | string |  |
| `applicantFirstNames` | string |  |
| `applicantFullName` | string |  |
| `applicantId` | string |  |
| `applicantLastName` | string |  |
| `changedAt` | date |  |
| `fromStage` | string |  |
| `id` | number |  |
| `jobId` | string |  |
| `jobTitle` | string |  |
| `toStage` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /stage/track` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application-stage-tracking.md) for the provider-specific parameters and requirements.

