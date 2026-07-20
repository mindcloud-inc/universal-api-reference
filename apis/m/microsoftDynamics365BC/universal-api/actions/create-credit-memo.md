# Microsoft Dynamics 365 BC: Create Credit Memo



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company_id` | string | yes |  |
| `customerNumber` | string | no |  |
| `externalDocumentNumber` | string | no |  |
| `creditMemoDate` | string | no |  |
| `postingDate` | string | no |  |
| `shortcutDimension1Code` | string | no |  |
| `shortcutDimension2Code` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `POST v2.0/companies(:company_id)/salesCreditMemos` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credit-memo.md) for the provider-specific parameters and requirements.

