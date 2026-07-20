# Raklet: Get Debt



```
GET https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-debt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-debt?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-debt?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "currency": 1,
      "debtType": 1,
      "description": "string",
      "id": "string",
      "isManuelEntry": true,
      "month": 1,
      "organisationMembershipId": "string",
      "status": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdOn` | date |  |
| `currency` | number |  |
| `debtType` | number |  |
| `description` | string |  |
| `id` | string |  |
| `isManuelEntry` | boolean |  |
| `month` | number |  |
| `organisationMembershipId` | string |  |
| `status` | number |  |
| `year` | number |  |

## Native endpoint

Through the native Raklet API, this operation is `GET /organisations/:organisationId/debts/:id` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-debt.md) for the provider-specific parameters and requirements.

