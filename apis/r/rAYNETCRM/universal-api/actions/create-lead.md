# RAYNET CRM: Create Lead



```
POST https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "priority": "string",
  "topic": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "priority": "string",
    "topic": "string"
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
| `priority` | string | yes | Lead priority. |
| `topic` | string | yes | Lead topic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native RAYNET CRM API, this operation is `PUT lead/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

