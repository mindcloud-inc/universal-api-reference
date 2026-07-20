# RAYNET CRM: Update Lead



```
PUT https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-lead', {
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
| `companyName` | string | no | Lead company name. |
| `contactInfo.email` | string | no | Lead email address. |
| `contactInfo.tel1` | string | no | Lead primary phone number. |
| `contactInfo.www` | string | no | Lead website URL. |
| `firstName` | string | no | Lead first name. |
| `lastName` | string | no | Lead last name. |
| `leadId` | string | yes | Raynet lead identifier. |
| `priority` | string | no | Lead priority. |
| `topic` | string | no | Lead topic. |

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

Through the native RAYNET CRM API, this operation is `POST lead/:leadId/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

