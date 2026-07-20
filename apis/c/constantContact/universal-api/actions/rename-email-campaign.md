# Constant Contact: Rename Email Campaign

Renames an email campaign in Constant Contact.

```
PUT https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/rename-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/rename-email-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "91569d46-00e4-4a4d-9a4c-d17d98740d04",
  "name": "Renamed campaign"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/rename-email-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "91569d46-00e4-4a4d-9a4c-d17d98740d04",
    "name": "Renamed campaign"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The unique identifier for an email campaign. Example: `91569d46-00e4-4a4d-9a4c-d17d98740d04`. |
| `name` | string | yes | Updated unique name for the email campaign. Example: `Renamed campaign`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignActivities": [
        {
          "campaignActivityId": "string",
          "role": "string"
        }
      ],
      "campaignId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentStatus": "string",
      "name": "Ava Chen",
      "type": "string",
      "typeCode": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignActivities` | array<object> |  |
| `campaignActivities[].campaignActivityId` | string |  |
| `campaignActivities[].role` | string |  |
| `campaignId` | string |  |
| `createdAt` | date |  |
| `currentStatus` | string |  |
| `name` | string |  |
| `type` | string |  |
| `typeCode` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Constant Contact API, this operation is `PATCH /emails/:campaign_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-email-campaign.md) for the provider-specific parameters and requirements.

