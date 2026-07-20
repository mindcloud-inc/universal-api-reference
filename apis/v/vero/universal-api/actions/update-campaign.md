# Vero: Update Campaign

Updates an existing campaign in Vero.

```
PUT https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "campaign_example"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-campaign', {
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
| `audience` | string | no | Optional audience reference update. |
| `id` | string | yes | The campaign identifier. Default: `campaign_example`. |
| `status` | string | no | Optional campaign status update. |
| `title` | string | no | Optional campaign title update. |
| `action` | object | no | Optional campaign action object update. |
| `trigger` | object | no | Optional trigger reference or expanded trigger object update. |
| `conversion` | object | no | Optional conversion object update. |
| `archived` | boolean | no | Optional archived flag update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "status": "string",
      "title": "string"
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
| `title` | string | Campaign title. |

## Native endpoint

Through the native Vero API, this operation is `PATCH /api/v4/campaigns/:id` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

