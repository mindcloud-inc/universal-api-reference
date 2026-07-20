# Constant Contact: Create Email Campaign

Creates an email campaign in Constant Contact.

```
POST https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-email-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "December Newsletter for Dog Lovers",
  "emailCampaignActivities[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-email-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "December Newsletter for Dog Lovers",
    "emailCampaignActivities[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Unique name for the email campaign. Example: `December Newsletter for Dog Lovers`. |
| `emailCampaignActivities[]` | array<object> | yes | Array containing the email campaign activity content object. |

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

Through the native Constant Contact API, this operation is `POST /emails` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-campaign.md) for the provider-specific parameters and requirements.

