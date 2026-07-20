# Platrum: Save counterparty

Creates or updates a counterparty in Platrum.

```
POST https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-counterparty
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-counterparty" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-counterparty', {
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
| `address` | string | no | Counterparty address. |
| `comment` | string | no | Counterparty comment. |
| `company_name` | string | no | Company name. |
| `email` | string | no | Counterparty email. |
| `id` | number | no | Counterparty ID for updates. |
| `name` | string | no | Counterparty name. |
| `phone` | string | no | Counterparty phone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Platrum API, this operation is `POST /fintransaction/api/counterparty/save` (base URL `https://3e8e7be.platrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-counterparty.md) for the provider-specific parameters and requirements.

