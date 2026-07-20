# AdvantShop: Create Lead

Creates a new lead in AdvantShop.

```
POST https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Lead description. |
| `firstName` | string | no | Lead first name. AdvantShop requires at least one of FirstName, Email, or Phone. |
| `email` | string | no | Lead email. AdvantShop requires at least one of FirstName, Email, or Phone. |
| `phone` | string | no | Lead phone. AdvantShop requires at least one of FirstName, Email, or Phone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "leadId": 1,
      "result": true,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `leadId` | number |  |
| `result` | boolean |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native AdvantShop API, this operation is `POST /leads/add` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

