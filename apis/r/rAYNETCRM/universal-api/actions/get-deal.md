# RAYNET CRM: Get Deal



```
GET https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID&businessCaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessCaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/get-deal?${params}`, {
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
| `businessCaseId` | string | yes | Raynet deal identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessCasePhase": {
        "value": "string"
      },
      "businessCaseType": {
        "value": "string"
      },
      "code": "string",
      "company": {
        "id": 1,
        "name": "Ava Chen"
      },
      "currency": {
        "value": "string"
      },
      "description": "string",
      "estimatedValue": 1,
      "id": 1,
      "name": "Ava Chen",
      "owner": {
        "fullName": "Ava Chen",
        "id": 1
      },
      "probability": 1,
      "rowInfo": {
        "createdAt": "string",
        "createdBy": "string"
      },
      "securityLevel": {
        "name": "Ava Chen"
      },
      "status": "string",
      "totalAmount": 1,
      "totalAmountWithTax": 1,
      "validFrom": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessCasePhase.value` | string | Current deal phase. |
| `businessCaseType.value` | string | Deal type. |
| `code` | string | Deal code. |
| `company.id` | number | Linked company identifier. |
| `company.name` | string | Linked company name. |
| `currency.value` | string | Deal currency symbol. |
| `description` | string | Deal description. |
| `estimatedValue` | number | Estimated deal value. |
| `id` | number | Raynet deal identifier. |
| `name` | string | Deal name. |
| `owner.fullName` | string | Assigned owner full name. |
| `owner.id` | number | Assigned owner identifier. |
| `probability` | number | Winning probability percentage. |
| `rowInfo.createdAt` | string | Record creation timestamp. |
| `rowInfo.createdBy` | string | Record creator label. |
| `securityLevel.name` | string | Assigned security level name. |
| `status` | string | Deal lifecycle status. |
| `totalAmount` | number | Deal total amount. |
| `totalAmountWithTax` | number | Deal total amount including tax. |
| `validFrom` | date | Deal validity start date. |

## Native endpoint

Through the native RAYNET CRM API, this operation is `GET businessCase/:businessCaseId/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

