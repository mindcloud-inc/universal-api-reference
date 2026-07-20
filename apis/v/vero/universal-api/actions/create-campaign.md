# Vero: Create Campaign

Creates a new campaign in Vero.

```
POST https://connect.mindcloud.co/v1/universal/vero/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vero/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "campaign_example",
  "object": "campaign",
  "title": "Example campaign",
  "action": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vero/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "campaign_example",
    "object": "campaign",
    "title": "Example campaign",
    "action": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audience` | string | no | Optional audience reference. |
| `id` | string | yes | The campaign identifier. Must match Vero's campaign_* pattern. Default: `campaign_example`. |
| `status` | string | no | Optional campaign status. |
| `object` | string | yes | The resource type. Vero documents this as campaign. Default: `campaign`. |
| `title` | string | yes | The internal campaign title. Default: `Example campaign`. |
| `action` | object | yes | The campaign action object. Default: `{}`. |
| `trigger` | object | no | Optional trigger reference or expanded trigger object. |
| `conversion` | object | no | Optional conversion object. |
| `archived` | boolean | no | Optional archived flag. |

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

Through the native Vero API, this operation is `POST /api/v4/campaigns` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

