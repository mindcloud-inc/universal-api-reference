# Rentman: Get Project



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-project?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Numeric Rentman project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_manager": "string",
      "already_invoiced": 1,
      "color": "string",
      "conditions": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "current": 1,
      "cust_contact": "string",
      "custom": {},
      "customer": "string",
      "deposit_status": "string",
      "displayname": "Ava Chen",
      "equipment_period_from": "2026-05-07T12:00:00.000Z",
      "equipment_period_to": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "loc_contact": "string",
      "location": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number": 1,
      "planperiod_end": "2026-05-07T12:00:00.000Z",
      "planperiod_start": "2026-05-07T12:00:00.000Z",
      "power": 1,
      "project_crew_price": 1,
      "project_insurance_price": 1,
      "project_other_price": 1,
      "project_rental_price": 1,
      "project_sale_price": 1,
      "project_total_price": 1,
      "project_total_price_cancelled": 1,
      "project_transport_price": 1,
      "project_type": "string",
      "purchasecosts": 1,
      "reference": "string",
      "refundabledeposit": 1,
      "tags": "string",
      "updateHash": "string",
      "usageperiod_end": "2026-05-07T12:00:00.000Z",
      "usageperiod_start": "2026-05-07T12:00:00.000Z",
      "volume": 1,
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_manager` | string |  |
| `already_invoiced` | number |  |
| `color` | string |  |
| `conditions` | string |  |
| `created` | date |  |
| `creator` | string |  |
| `current` | number |  |
| `cust_contact` | string |  |
| `custom` | object |  |
| `customer` | string |  |
| `deposit_status` | string |  |
| `displayname` | string |  |
| `equipment_period_from` | date |  |
| `equipment_period_to` | date |  |
| `id` | number |  |
| `loc_contact` | string |  |
| `location` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `number` | number |  |
| `planperiod_end` | date |  |
| `planperiod_start` | date |  |
| `power` | number |  |
| `project_crew_price` | number |  |
| `project_insurance_price` | number |  |
| `project_other_price` | number |  |
| `project_rental_price` | number |  |
| `project_sale_price` | number |  |
| `project_total_price` | number |  |
| `project_total_price_cancelled` | number |  |
| `project_transport_price` | number |  |
| `project_type` | string |  |
| `purchasecosts` | number |  |
| `reference` | string |  |
| `refundabledeposit` | number |  |
| `tags` | string |  |
| `updateHash` | string |  |
| `usageperiod_end` | date |  |
| `usageperiod_start` | date |  |
| `volume` | number |  |
| `weight` | number |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /projects/:id` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

