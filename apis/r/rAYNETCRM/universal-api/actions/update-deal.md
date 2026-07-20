# RAYNET CRM: Update Deal



```
PUT https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessCaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessCaseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessCaseId` | string | yes | Raynet deal identifier. |
| `company` | number | no | Linked company identifier. |
| `description` | string | no | Deal description. |
| `estimatedValue` | number | no | Estimated deal value. |
| `name` | string | no | Deal name. |
| `totalAmount` | number | no | Deal total amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | string |  |

## Native endpoint

Through the native RAYNET CRM API, this operation is `POST businessCase/:businessCaseId/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

