# Vero: Launch Campaign

Launches an existing campaign in Vero.

```
PUT https://connect.mindcloud.co/v1/universal/vero/latest/actions/launch-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vero/latest/actions/launch-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "campaign_example"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vero/latest/actions/launch-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "campaign_example"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The campaign identifier. Default: `campaign_example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Campaign identifier. |
| `object` | string | Resource type. |
| `status` | string | Campaign status. |

## Native endpoint

Through the native Vero API, this operation is `POST /api/v4/campaigns/:id/launch` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/launch-campaign.md) for the provider-specific parameters and requirements.

