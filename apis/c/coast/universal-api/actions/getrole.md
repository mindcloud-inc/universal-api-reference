# Coast: Get Role By ID



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getrole
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getrole?connectionId=$CONNECTION_ID&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getrole?${params}`, {
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
| `roleId` | string | yes | Coast role ID of the role to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "permissions": {
        "addBankAccountsAndMakePayments": true,
        "approvePolicyExceptionRequests": true,
        "cancelCards": true,
        "createAndEditBills": true,
        "createAndEditPeopleAndVehicles": true,
        "createAndEditPolicies": true,
        "createVirtualCards": true,
        "installAndUninstallIntegrations": true,
        "manageCardAssignments": true,
        "managePolicyAssignments": true,
        "orderPhysicalCards": true,
        "viewAndExportStatements": true,
        "viewAndManageAccount": true,
        "viewCards": true,
        "viewPeopleAndVehicles": true,
        "viewPolicies": true
      },
      "roleType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `permissions.addBankAccountsAndMakePayments` | boolean |  |
| `permissions.approvePolicyExceptionRequests` | boolean |  |
| `permissions.cancelCards` | boolean |  |
| `permissions.createAndEditBills` | boolean |  |
| `permissions.createAndEditPeopleAndVehicles` | boolean |  |
| `permissions.createAndEditPolicies` | boolean |  |
| `permissions.createVirtualCards` | boolean |  |
| `permissions.installAndUninstallIntegrations` | boolean |  |
| `permissions.manageCardAssignments` | boolean |  |
| `permissions.managePolicyAssignments` | boolean |  |
| `permissions.orderPhysicalCards` | boolean |  |
| `permissions.viewAndExportStatements` | boolean |  |
| `permissions.viewAndManageAccount` | boolean |  |
| `permissions.viewCards` | boolean |  |
| `permissions.viewPeopleAndVehicles` | boolean |  |
| `permissions.viewPolicies` | boolean |  |
| `roleType` | string |  |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/roles/:roleId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getrole.md) for the provider-specific parameters and requirements.

