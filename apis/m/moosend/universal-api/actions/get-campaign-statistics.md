# Moosend: Get Campaign Statistics

Retrieves campaign statistics from Moosend.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-statistics?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-statistics?${params}`, {
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
| `campaignId` | string | yes | The ID of the campaign that you are fetching statistics for. |
| `type` | string | no | The type of activity used to get information and display statistics. Possible values are: Sent - when and to which recipients the campaign was sent. Opened - who opened the campaign. LinkClicked - who clicked on which links in the campaign. Unsubscribed - who unsubscribed from the campaign by clicking the unsubscribe link and when. Bounced - which email recipients failed to receive the campaign. If not specified, Sent value is used by default. Complained - which email recipients reported your campaign as spam through their email service. Activity - all types of activities for the campaign. |
| `date` | date | no | The specific year, month, and day the activity occurred. The date has a YYYY/MM/DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "contextDescription": "string",
      "contextName": "Ava Chen",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "totalCount": 1,
      "uniqueCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string |  |
| `contextDescription` | string |  |
| `contextName` | string |  |
| `timestamp` | date |  |
| `totalCount` | number |  |
| `uniqueCount` | number |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /campaigns/{{CampaignID}}/stats/{{Type}}.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-statistics.md) for the provider-specific parameters and requirements.

