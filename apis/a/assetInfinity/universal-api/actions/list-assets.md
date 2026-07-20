# Asset Infinity: List Assets

Retrieves assets from Asset Infinity.

```
GET https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Infinity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-assets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "allotedTo": "string",
          "assDescription": "string",
          "assetCode": "string",
          "assetId": 1,
          "assetName": "Ava Chen",
          "brand": "string",
          "capitalizationDate": "2026-05-07T12:00:00.000Z",
          "capitalizationPrice": 1,
          "categoryId": "string",
          "conditionId": "string",
          "createdBy": "string",
          "createdDate": "2026-05-07T12:00:00.000Z",
          "deprecationPct": 1,
          "endofLife": "2026-05-07T12:00:00.000Z",
          "formId": 1,
          "invoiceNo": "string",
          "isBle": 1,
          "isParent": 1,
          "isParentTransfer": 1,
          "isPartner": true,
          "isViewItAsset": 1,
          "isWorkflow": 1,
          "locationId": "string",
          "model": "string",
          "modifiedBy": "string",
          "modifiedDate": "2026-05-07T12:00:00.000Z",
          "poNumber": "string",
          "purchaseDate": "2026-05-07T12:00:00.000Z",
          "referenceId": 1,
          "remarks": "string",
          "reservationState": 1,
          "rowColor": "string",
          "rowIndexNumber": 1,
          "serialNo": "string",
          "statusId": "string",
          "tParent": "string",
          "transactionApprovalDetailId": 1,
          "userName": "Ava Chen"
        }
      ],
      "isSuccess": true,
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].allotedTo` | string |  |
| `data[].assDescription` | string |  |
| `data[].assetCode` | string |  |
| `data[].assetId` | number |  |
| `data[].assetName` | string |  |
| `data[].brand` | string |  |
| `data[].capitalizationDate` | date |  |
| `data[].capitalizationPrice` | number |  |
| `data[].categoryId` | string |  |
| `data[].conditionId` | string |  |
| `data[].createdBy` | string |  |
| `data[].createdDate` | date |  |
| `data[].deprecationPct` | number |  |
| `data[].endofLife` | date |  |
| `data[].formId` | number |  |
| `data[].invoiceNo` | string |  |
| `data[].isBle` | number |  |
| `data[].isParent` | number |  |
| `data[].isParentTransfer` | number |  |
| `data[].isPartner` | boolean |  |
| `data[].isViewItAsset` | number |  |
| `data[].isWorkflow` | number |  |
| `data[].locationId` | string |  |
| `data[].model` | string |  |
| `data[].modifiedBy` | string |  |
| `data[].modifiedDate` | date |  |
| `data[].poNumber` | string |  |
| `data[].purchaseDate` | date |  |
| `data[].referenceId` | number |  |
| `data[].remarks` | string |  |
| `data[].reservationState` | number |  |
| `data[].rowColor` | string |  |
| `data[].rowIndexNumber` | number |  |
| `data[].serialNo` | string |  |
| `data[].statusId` | string |  |
| `data[].tParent` | string |  |
| `data[].transactionApprovalDetailId` | number |  |
| `data[].userName` | string |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Asset Infinity API, this operation is `POST asset-list` (base URL `https://api.assetinfinity.io/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

