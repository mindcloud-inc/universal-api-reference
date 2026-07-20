# lemlist: Update Campaign

Updates an existing campaign in lemlist.

```
PUT https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "67618ad126d28d06429eb1c4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "67618ad126d28d06429eb1c4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The ID of the campaign to update. Example: `67618ad126d28d06429eb1c4`. |
| `name` | string | no | The updated campaign name. Example: `MindCloud Stage 3 Test Campaign`. |
| `stopOnEmailReplied` | boolean | no | Pause or stop the campaign when a lead replies by email. |
| `stopOnMeetingBooked` | boolean | no | Pause or stop the campaign when a meeting is booked. |
| `stopOnLinkClicked` | boolean | no | Pause or stop the campaign when a lead clicks a link. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stopOnLinkClickedFilter` | string | no | Restrict the link-click stop rule using the documented filter value. Example: `message_only`. |
| `leadsPausedByInterest` | boolean | no | Pause leads automatically when they are marked as interested. |
| `opportunityReplied` | boolean | no | Update the campaign opportunity stage when a reply is received. |
| `opportunityClicked` | boolean | no | Update the campaign opportunity stage when a tracked link is clicked. |
| `autoLeadInterest` | boolean | no | Automatically score or infer lead interest from campaign activity. |
| `disableTrackOpen` | boolean | no | Disable open tracking for this campaign. |
| `disableTrackClick` | boolean | no | Disable click tracking for this campaign. |
| `disableTrackReply` | boolean | no | Disable reply tracking for this campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "stopOnEmailReplied": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `stopOnEmailReplied` | boolean |  |

## Native endpoint

Through the native lemlist API, this operation is `PATCH /campaigns/:campaignId` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

