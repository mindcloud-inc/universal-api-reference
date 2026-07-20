# RD Station Marketing: Get Email Marketing Statistics



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-email-marketing-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-email-marketing-statistics?connectionId=$CONNECTION_ID&endDate=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-email-marketing-statistics?${params}`, {
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
| `endDate` | string | yes | End date for analytics range (YYYY-MM-DD). |
| `startDate` | string | yes | Start date for analytics range (YYYY-MM-DD). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "emails": [
        {
          "campaignId": 1,
          "campaignName": "ava@example.com",
          "contactsCount": 1,
          "emailClickedCount": 1,
          "emailDeliveredCount": 1,
          "emailOpenedCount": 1,
          "emailUnsubscribedCount": 1,
          "sendAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "queryDate": {
        "endDate": "2026-05-07T12:00:00.000Z",
        "startDate": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `emails[].campaignId` | number |  |
| `emails[].campaignName` | string |  |
| `emails[].contactsCount` | number |  |
| `emails[].emailClickedCount` | number |  |
| `emails[].emailDeliveredCount` | number |  |
| `emails[].emailOpenedCount` | number |  |
| `emails[].emailUnsubscribedCount` | number |  |
| `emails[].sendAt` | date |  |
| `queryDate.endDate` | date |  |
| `queryDate.startDate` | date |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `GET /platform/analytics/emails` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-marketing-statistics.md) for the provider-specific parameters and requirements.

