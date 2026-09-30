# Microsoft Dynamics 365: Create Project Contract



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ProjectContractID": "string",
  "Name": "Ava Chen",
  "ContractDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ProjectContractID": "string",
    "Name": "Ava Chen",
    "ContractDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataAreaId` | string | no |  |
| `ProjectContractID` | string | yes |  |
| `Name` | string | yes |  |
| `ContractDate` | date | yes |  |
| `SalesTaxGroup` | string | no |  |
| `ContractLines` | string | no | Yes/No Default: `Yes`. |
| `BankAccount` | string | no |  |
| `InvoicingName` | string | no |  |
| `LockContractSalesCurrency` | string | no | Yes/No Default: `Yes`. |
| `CentralBankPurposeCode` | string | no |  |
| `SalesResponsiblePersonnelNumber` | string | no |  |
| `PriceGroup` | string | no |  |
| `NetPrice` | string | no | Default: `No`. |
| `PurposeText` | string | no |  |
| `InvoiceFrequency` | string | no | "CurrentMth" Default: `CurrentMth`. |
| `SalesCurrency` | string | no | Default: `USD`. |
| `DefaultPostingLevel` | string | no | Default: `Detail`. |
| `TransactionCode` | string | no |  |
| `RetainagePercent` | number | no | Default: `0`. |
| `MinimumTimeIncrement` | number | no | Default: `0`. |
| `ServiceOnDeliveryAddress` | string | no | Default: `No`. |
| `CustomerRetentionTermId` | string | no |  |
| `ListCodeId` | string | no | Default: `IncludeNot`. |
| `ProgressInvoicing` | boolean | no | Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `POST ProjectContracts` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-contract.md) for the provider-specific parameters and requirements.

