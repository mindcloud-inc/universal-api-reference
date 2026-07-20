# RAYNET CRM: Update Company



```
PUT https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | Raynet company identifier. |
| `name` | string | no | [Name] |
| `rating` | string | no | [Rating] |
| `state` | string | no | [Status] |
| `role` | string | no | [Relationship] |
| `notice` | string | no | [Note to account] |
| `regNumber` | string | no | [ID no.] |
| `taxNumber` | string | no | [Tax ID no.] |

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

Through the native RAYNET CRM API, this operation is `POST company/:companyId/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

