# RAYNET CRM: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "personId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "personId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | string | yes | contact ID |
| `firstName` | string | no | [Name] |
| `lastName` | string | no | [Last name] |
| `contactInfo.email` | string | no | [Email] |
| `contactInfo.tel1` | string | no | [Phone 1] |
| `contactInfo.www` | string | no | [WWW] |

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

Through the native RAYNET CRM API, this operation is `POST person/:personId/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

