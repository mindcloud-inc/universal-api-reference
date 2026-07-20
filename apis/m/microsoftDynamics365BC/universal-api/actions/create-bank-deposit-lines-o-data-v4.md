# Microsoft Dynamics 365 BC: Create Bank Deposit Lines ODataV4



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-bank-deposit-lines-o-data-v4
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-bank-deposit-lines-o-data-v4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-bank-deposit-lines-o-data-v4', {
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
| `company` | list | no |  |
| `Bank_Deposit_No` | string | no |  |
| `Account_Type` | string | no |  |
| `Account_No` | string | no |  |
| `Document_Type` | string | no |  |
| `Document_No` | string | no |  |
| `External_Document_No` | string | no |  |
| `Description` | string | no |  |
| `Credit_Amount` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudBankDepositLines` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bank-deposit-lines-o-data-v4.md) for the provider-specific parameters and requirements.

