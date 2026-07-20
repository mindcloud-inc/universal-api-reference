# Routee: Track multiple messages for a specific bulk send out - campaign

Tracks multiple messages for a specific bulk send out - campaign in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-messages-for-a-specific-bulk-send-out-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-messages-for-a-specific-bulk-send-out-campaign?connectionId=$CONNECTION_ID&campaignTrackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignTrackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-messages-for-a-specific-bulk-send-out-campaign?${params}`, {
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
| `campaignTrackingId` | string | yes | The tracking id of the campaign which includes the messages. |
| `page` | string | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | string | no | The number of items to retrieve, default value is 20. Max value is 2000. |
| `sort` | string | no | The field name that will be used to sort the results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        [
          {}
        ]
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].applicationName` | string |  |
| `content[].body` | string |  |
| `content[].campaignName` | string |  |
| `content[].country` | string |  |
| `content[].direction` | string |  |
| `content[].from` | string |  |
| `content[].groups[]` | array |  |
| `content[].latency` | number |  |
| `content[].messageId` | string |  |
| `content[].operator` | string |  |
| `content[].originatingService` | string |  |
| `content[].part` | number |  |
| `content[].parts` | number |  |
| `content[].price` | number |  |
| `content[].smsId` | string |  |
| `content[].status` | object |  |
| `content[].status.date` | string |  |
| `content[].status.reason` | object |  |
| `content[].status.reason.description` | string |  |
| `content[].status.reason.detailedStatus` | string |  |
| `content[].status.status` | string |  |
| `content[].to` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /sms/tracking/campaign/:campaignTrackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-multiple-messages-for-a-specific-bulk-send-out-campaign.md) for the provider-specific parameters and requirements.

