# Maildrip: Add an email to a campaign



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-an-email-to-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-an-email-to-a-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-an-email-to-a-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of the campaign to add an email to |
| `subject` | string | no |  |
| `body` | string | no |  |
| `typeOfMail` | string | no |  |
| `emailInterval` | number | no |  |
| `selectTemplate` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/campaigns/{campaignId}/addmail` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-an-email-to-a-campaign.md) for the provider-specific parameters and requirements.

