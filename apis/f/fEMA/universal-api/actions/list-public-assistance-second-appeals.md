# FEMA: List Public Assistance Second Appeals

Retrieves public assistance second appeals from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-second-appeals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-second-appeals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-second-appeals?${params}`, {
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
      "appellant": "string",
      "applicantId": "string",
      "decisionSignedDate": "2026-05-07T12:00:00.000Z",
      "declarationType": "string",
      "disasterNumber": "string",
      "emailAcknowledgementDate": "2026-05-07T12:00:00.000Z",
      "hqReceivedDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "pwgmpNumber": "string",
      "recipient": "string",
      "region": 1,
      "rfiDueDate": "2026-05-07T12:00:00.000Z",
      "rfiReceivedDate": "2026-05-07T12:00:00.000Z",
      "rfiSentDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appellant` | string |  |
| `applicantId` | string |  |
| `decisionSignedDate` | date |  |
| `declarationType` | string |  |
| `disasterNumber` | string |  |
| `emailAcknowledgementDate` | date |  |
| `hqReceivedDate` | date |  |
| `id` | number |  |
| `pwgmpNumber` | string |  |
| `recipient` | string |  |
| `region` | number |  |
| `rfiDueDate` | date |  |
| `rfiReceivedDate` | date |  |
| `rfiSentDate` | date |  |
| `status` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/PublicAssistanceSecondAppealsTracker` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-public-assistance-second-appeals.md) for the provider-specific parameters and requirements.

