# Routee: Retrieve Voice Trackings by Campaign

Retrieves voice trackings by campaign from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-voice-trackings-by-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-voice-trackings-by-campaign?connectionId=$CONNECTION_ID&campaignTrackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignTrackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-voice-trackings-by-campaign?${params}`, {
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
| `page` | string | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | string | no | The number of items to retrieve, default value is 20. |
| `sort` | string | no | The field name that will be used to sort the results. |
| `campaignTrackingId` | string | yes | The tracking id of the campaign which includes the messages. |

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
| `content[].campaign` | string |  |
| `content[].chargeInterval` | number |  |
| `content[].country` | string |  |
| `content[].direction` | string |  |
| `content[].duration` | number |  |
| `content[].fileURL` | string |  |
| `content[].from` | string |  |
| `content[].messageId` | string |  |
| `content[].originatingService` | string |  |
| `content[].price` | number |  |
| `content[].recordings[]` | array |  |
| `content[].status` | object |  |
| `content[].status.date` | string |  |
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

Through the native Routee API, this operation is `GET /voice/tracking/campaign/:campaignTrackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-voice-trackings-by-campaign.md) for the provider-specific parameters and requirements.

