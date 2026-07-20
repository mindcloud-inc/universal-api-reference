# Sendloop: Update Campaign



```
PUT https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | number | yes | ID number of the target campaign |
| `campaignName` | string | no | Name of your campaign |
| `fromName` | string | no | The name shown in the from email header |
| `fromEmail` | string | no | Sender email address |
| `replyToName` | string | no | The name shown in the reply-to header |
| `replyToEmail` | string | no | Email address to receive replies |
| `targetListIds` | string | no | ID numbers of recipient lists |
| `subject` | string | no | Subject of your email campaign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /campaign.update/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

