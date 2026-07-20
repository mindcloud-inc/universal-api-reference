# Datalyse: Create Email Template

Creates a new email template in Datalyse.

```
POST https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-email-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-email-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | Template HTML content |
| `name` | string | yes | Template name |
| `subject` | string | no | Default email subject (optional) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API response status |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/emails/templates/create.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-template.md) for the provider-specific parameters and requirements.

