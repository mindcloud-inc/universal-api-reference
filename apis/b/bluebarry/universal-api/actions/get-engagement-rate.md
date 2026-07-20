# Bluebarry: Get Engagement Rate

Retrieves engagement rate analytics from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-engagement-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-engagement-rate?connectionId=$CONNECTION_ID&advisorId=string&endDate=2026-05-07T12%3A00%3A00.000Z&questionId=string&startDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "advisorId": "string",
  "endDate": "2026-05-07T12:00:00.000Z",
  "questionId": "string",
  "startDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-engagement-rate?${params}`, {
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
| `advisorId` | string | yes |  |
| `endDate` | date | yes |  |
| `questionId` | string | yes |  |
| `startDate` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formattedValue": "string",
      "measureCount": "string",
      "totalCount": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formattedValue` | string |  |
| `measureCount` | string |  |
| `totalCount` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Bluebarry API, this operation is `GET /data/GetEngagementRate(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-engagement-rate.md) for the provider-specific parameters and requirements.

