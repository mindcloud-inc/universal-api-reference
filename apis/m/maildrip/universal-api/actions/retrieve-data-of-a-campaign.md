# Maildrip: Retrieve data of a campaign



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-data-of-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-data-of-a-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-data-of-a-campaign?${params}`, {
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
| `campaignId` | string | yes | ID of the campaign to retrieve data from |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "interval": 1,
      "name": "Ava Chen",
      "status": true,
      "variables": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | The unique identifier of the campaign |
| `interval` | number | The interval of the campaign |
| `name` | string | The name of the campaign |
| `status` | boolean | The status of the campaign |
| `variables` | array<string> | The variables of the campaign |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/campaigns/{campaign_id}/get-data` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-data-of-a-campaign.md) for the provider-specific parameters and requirements.

