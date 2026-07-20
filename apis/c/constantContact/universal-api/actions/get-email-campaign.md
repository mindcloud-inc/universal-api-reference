# Constant Contact: Get Email Campaign

Retrieves an email campaign from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign?connectionId=$CONNECTION_ID&campaignId=91569d46-00e4-4a4d-9a4c-d17d98740d04" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "91569d46-00e4-4a4d-9a4c-d17d98740d04"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign?${params}`, {
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
| `campaignId` | string | yes | The UUID that uniquely identifies the email campaign. Example: `91569d46-00e4-4a4d-9a4c-d17d98740d04`. |

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

Through the native Constant Contact API, this operation is `GET /emails/:campaign_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-campaign.md) for the provider-specific parameters and requirements.

