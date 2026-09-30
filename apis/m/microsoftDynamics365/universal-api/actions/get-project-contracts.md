# Microsoft Dynamics 365: Get Project Contracts



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-project-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-project-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-project-contracts?${params}`, {
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
| `$filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string",
        "etag": "string"
      },
      "BankAccount": "string",
      "CentralBankPurposeCode": "string",
      "ContractDate": "string",
      "ContractLines": "string",
      "CustomerRetentionTermId": "string",
      "dataAreaId": "string",
      "DefaultPostingLevel": "string",
      "InvoiceFrequency": "string",
      "InvoicingName": "Ava Chen",
      "ListCodeId": "string",
      "LockContractSalesCurrency": "string",
      "MinimumTimeIncrement": 1,
      "Name": "Ava Chen",
      "NetPrice": "string",
      "PriceGroup": "string",
      "ProgressInvoicing": true,
      "ProjectContractID": "string",
      "PurposeText": "string",
      "RetainagePercent": 1,
      "SalesCurrency": "string",
      "SalesResponsiblePersonnelNumber": "string",
      "SalesTaxGroup": "string",
      "ServiceOnDeliveryAddress": "string",
      "TransactionCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string |  |
| `@odata.etag` | string |  |
| `BankAccount` | string |  |
| `CentralBankPurposeCode` | string |  |
| `ContractDate` | string |  |
| `ContractLines` | string |  |
| `CustomerRetentionTermId` | string |  |
| `dataAreaId` | string |  |
| `DefaultPostingLevel` | string |  |
| `InvoiceFrequency` | string |  |
| `InvoicingName` | string |  |
| `ListCodeId` | string |  |
| `LockContractSalesCurrency` | string |  |
| `MinimumTimeIncrement` | number |  |
| `Name` | string |  |
| `NetPrice` | string |  |
| `PriceGroup` | string |  |
| `ProgressInvoicing` | boolean |  |
| `ProjectContractID` | string |  |
| `PurposeText` | string |  |
| `RetainagePercent` | number |  |
| `SalesCurrency` | string |  |
| `SalesResponsiblePersonnelNumber` | string |  |
| `SalesTaxGroup` | string |  |
| `ServiceOnDeliveryAddress` | string |  |
| `TransactionCode` | string |  |

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `GET ProjectContracts` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-contracts.md) for the provider-specific parameters and requirements.

