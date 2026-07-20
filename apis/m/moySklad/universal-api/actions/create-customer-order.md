# MoySklad: Create customer order

Creates a customer order in MoySklad.

```
POST https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-customer-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-customer-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agent.meta.href": "https://api.moysklad.ru/api/remap/1.2/entity/counterparty/895e1d49-3cd0-11f1-0a80-0f8100398133",
  "agent.meta.mediaType": "application/json",
  "agent.meta.type": "counterparty",
  "name": "MindCloud Validator Order",
  "organization.meta.href": "https://api.moysklad.ru/api/remap/1.2/entity/organization/895bd002-3cd0-11f1-0a80-0f810039812f",
  "organization.meta.mediaType": "application/json",
  "organization.meta.type": "organization"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-customer-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agent.meta.href": "https://api.moysklad.ru/api/remap/1.2/entity/counterparty/895e1d49-3cd0-11f1-0a80-0f8100398133",
    "agent.meta.mediaType": "application/json",
    "agent.meta.type": "counterparty",
    "name": "MindCloud Validator Order",
    "organization.meta.href": "https://api.moysklad.ru/api/remap/1.2/entity/organization/895bd002-3cd0-11f1-0a80-0f810039812f",
    "organization.meta.mediaType": "application/json",
    "organization.meta.type": "organization"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agent.meta.href` | string | yes | MoySklad agent.meta.href argument. Default: `https://api.moysklad.ru/api/remap/1.2/entity/counterparty/895e1d49-3cd0-11f1-0a80-0f8100398133`. |
| `agent.meta.mediaType` | string | yes | MoySklad agent.meta.mediaType argument. Default: `application/json`. |
| `agent.meta.type` | string | yes | MoySklad agent.meta.type argument. Default: `counterparty`. |
| `name` | string | yes | MoySklad name argument. Default: `MindCloud Validator Order`. |
| `organization.meta.href` | string | yes | MoySklad organization.meta.href argument. Default: `https://api.moysklad.ru/api/remap/1.2/entity/organization/895bd002-3cd0-11f1-0a80-0f810039812f`. |
| `organization.meta.mediaType` | string | yes | MoySklad organization.meta.mediaType argument. Default: `application/json`. |
| `organization.meta.type` | string | yes | MoySklad organization.meta.type argument. Default: `organization`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "moment": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "sum": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `moment` | date |  |
| `name` | string |  |
| `sum` | number |  |

## Native endpoint

Through the native MoySklad API, this operation is `POST entity/customerorder` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-order.md) for the provider-specific parameters and requirements.

