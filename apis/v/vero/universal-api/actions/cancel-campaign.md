# Vero: Cancel Campaign

Cancels an existing campaign in Vero.

```
DELETE https://connect.mindcloud.co/v1/universal/vero/latest/actions/cancel-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vero/latest/actions/cancel-campaign?connectionId=$CONNECTION_ID&id=campaign_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "campaign_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vero/latest/actions/cancel-campaign?${params}`, {
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

Through the native Vero API, this operation is `DELETE /api/v4/campaigns/:id/cancel` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-campaign.md) for the provider-specific parameters and requirements.

