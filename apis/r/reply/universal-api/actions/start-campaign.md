# Reply: Start Campaign



```
PUT https://connect.mindcloud.co/v1/universal/reply/latest/actions/start-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reply/latest/actions/start-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reply/latest/actions/start-campaign', {
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
| `campaignId` | number | yes | Reply campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "emailAccount": "ava@example.com",
      "id": 1,
      "isArchived": true,
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Campaign creation timestamp. |
| `emailAccount` | string | Selected sending email account. |
| `id` | number | Reply campaign identifier. |
| `isArchived` | boolean | Whether the campaign is archived. |
| `name` | string | Campaign name. |
| `status` | string | Campaign lifecycle status after starting. |

## Native endpoint

Through the native Reply API, this operation is `POST /v2/campaigns/:campaignId/start` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-campaign.md) for the provider-specific parameters and requirements.

