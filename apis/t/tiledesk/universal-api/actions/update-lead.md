# Tiledesk: Update Lead

Updates a lead in the current Tiledesk project.

```
PUT https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | The lead identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "fullname": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `fullname` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Tiledesk API, this operation is `PUT /{{credentials.projectId}}/leads/:leadId` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

