# BoardCRM: Update Lead

Updates an existing lead in BoardCRM.

```
PUT https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Lead ID. |
| `name` | string | no | Updated lead name. |
| `email` | string | no | Updated lead email. |
| `phone` | string | no | Updated lead phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "add_phone": "string",
      "created_at": "string",
      "email": "ava@example.com",
      "facebook": "string",
      "id": 1,
      "name": "Ava Chen",
      "note": "string",
      "organization": "string",
      "phone": "string",
      "position": "string",
      "skype": "string",
      "telegram": "string",
      "vk": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `add_phone` | string |  |
| `created_at` | string |  |
| `email` | string |  |
| `facebook` | string |  |
| `id` | number |  |
| `name` | string |  |
| `note` | string |  |
| `organization` | string |  |
| `phone` | string |  |
| `position` | string |  |
| `skype` | string |  |
| `telegram` | string |  |
| `vk` | string |  |
| `website` | string |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /lead/update` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

