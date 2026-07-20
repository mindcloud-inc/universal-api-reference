# Callingly: Update Lead

Updates a lead in Callingly.

```
PUT https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "leadId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "leadId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | The lead company. |
| `email` | string | no | The lead email address. |
| `firstName` | string | no | The lead first name. |
| `id` | number | yes | The Callingly lead ID to update. |
| `isBlocked` | number | no | Whether the lead is blocked. |
| `isStopped` | number | no | Whether the lead is stopped. |
| `lastName` | string | no | The lead last name. |
| `leadId` | number | yes | The lead ID in the request body, as shown in the docs sample. |
| `phoneNumber` | string | no | The lead phone number. |
| `result` | string | no | The lead result. |
| `source` | string | no | The lead source. |
| `stage` | string | no | The lead stage. |
| `status` | string | no | The lead status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Callingly API, this operation is `PUT /v1/leads/{{id}}` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

