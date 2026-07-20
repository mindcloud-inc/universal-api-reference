# Sarbacane: Create Email Campaign

Creates a new email campaign in Sarbacane.

```
POST https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/create-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/create-email-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/create-email-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aliasFrom` | string | no | Sender display name. |
| `aliasReplyTo` | string | no | Reply-to display name. |
| `emailFrom` | string | no | Sender email address. |
| `emailReplyTo` | string | no | Reply-to email address. |
| `name` | string | no | Campaign name. |
| `preheader` | string | no | Campaign preheader text. |
| `subject` | string | no | Campaign subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created campaign ID. |
| `name` | string | Campaign name. |

## Native endpoint

Through the native Sarbacane API, this operation is `POST /campaigns/email` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-campaign.md) for the provider-specific parameters and requirements.

