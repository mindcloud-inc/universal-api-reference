# Zoho ZeptoMail: Add Suppression

Adds a suppression list entry in Zoho ZeptoMail.

```
POST https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-suppression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-suppression" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "action": "string",
  "values[0]": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-suppression', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "action": "string",
    "values[0]": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Suppression category to manage. |
| `action` | string | yes | Suppression action: reject, suppress, or suppress_tracking. |
| `values[0]` | string | yes | Email address or domain to suppress. |
| `description` | string | no | Reason for the suppression entry. |
| `mailagent_keys[0]` | string | no | Agent alias to apply the suppression to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "action": "string",
        "description": "string",
        "mailagent_keys": [
          "string"
        ],
        "modified_time": "2026-05-07T12:00:00.000Z",
        "value": "string"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.action` | string |  |
| `data.description` | string |  |
| `data.mailagent_keys[]` | string |  |
| `data.modified_time` | date |  |
| `data.value` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `POST suppressions/:type` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-suppression.md) for the provider-specific parameters and requirements.

