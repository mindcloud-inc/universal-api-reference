# Proofly: Toggle Campaign

Toggles a campaign between active and inactive in Proofly.

```
PUT https://connect.mindcloud.co/v1/universal/proofly/latest/actions/toggle-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Proofly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/proofly/latest/actions/toggle-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proofly/latest/actions/toggle-campaign', {
  method: 'PUT',
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
| `campaignId` | string | yes | The campaign ID from List Campaigns. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Toggle confirmation message |

## Native endpoint

Through the native Proofly API, this operation is `PUT /campaign/:campaignId` (base URL `https://proofly.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/toggle-campaign.md) for the provider-specific parameters and requirements.

