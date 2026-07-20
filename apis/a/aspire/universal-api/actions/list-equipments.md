# Aspire: List Equipments



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipments?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "approvedDate": "string",
      "approvedUserID": 1,
      "approvedUserName": "Ava Chen",
      "aspireGPSIdentifier": "string",
      "assetNumber": "string",
      "branchID": 1,
      "branchName": "Ava Chen",
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "dealer": {},
      "description": "string",
      "disposedDate": {},
      "disposedPrice": {},
      "disposedUserID": {},
      "disposedUserName": {},
      "divisionID": 1,
      "divisionName": "Ava Chen",
      "engineNumber": {},
      "equipmentDisposalReason": {},
      "equipmentDisposalReasonID": {},
      "equipmentID": 1,
      "equipmentModelID": 1,
      "equipmentModelName": "Ava Chen",
      "equipmentStatusID": 1,
      "equipmentStatusName": "Ava Chen",
      "estimatedPurchasePrice": 1,
      "financingBank": {},
      "grossVehicleWeight": 1,
      "inServiceDate": "string",
      "inServiceUserID": 1,
      "inServiceUserName": "Ava Chen",
      "lastModifiedByUserID": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastModifiedDateTime": "string",
      "mileageHours": 1,
      "modelYear": 1,
      "outOfServiceDate": {},
      "outOfServiceUserID": {},
      "outOfServiceUserName": {},
      "paySchedule": 1,
      "plateNumber": "string",
      "propertyID": {},
      "propertyName": {},
      "purchasedDate": "string",
      "purchasedUserID": 1,
      "purchasedUserName": "Ava Chen",
      "purchasePrice": 1,
      "renewalDate": "string",
      "requestedDate": "string",
      "requestedUserID": 1,
      "requestedUserName": "Ava Chen",
      "routeID": {},
      "routeName": {},
      "serialNumber": "string",
      "trackerType": "string",
      "warrantyDays": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `approvedDate` | string |  |
| `approvedUserID` | number |  |
| `approvedUserName` | string |  |
| `aspireGPSIdentifier` | string |  |
| `assetNumber` | string |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `dealer` | object |  |
| `description` | string |  |
| `disposedDate` | object |  |
| `disposedPrice` | object |  |
| `disposedUserID` | object |  |
| `disposedUserName` | object |  |
| `divisionID` | number |  |
| `divisionName` | string |  |
| `engineNumber` | object |  |
| `equipmentDisposalReason` | object |  |
| `equipmentDisposalReasonID` | object |  |
| `equipmentID` | number |  |
| `equipmentModelID` | number |  |
| `equipmentModelName` | string |  |
| `equipmentStatusID` | number |  |
| `equipmentStatusName` | string |  |
| `estimatedPurchasePrice` | number |  |
| `financingBank` | object |  |
| `grossVehicleWeight` | number |  |
| `inServiceDate` | string |  |
| `inServiceUserID` | number |  |
| `inServiceUserName` | string |  |
| `lastModifiedByUserID` | number |  |
| `lastModifiedByUserName` | string |  |
| `lastModifiedDateTime` | string |  |
| `mileageHours` | number |  |
| `modelYear` | number |  |
| `outOfServiceDate` | object |  |
| `outOfServiceUserID` | object |  |
| `outOfServiceUserName` | object |  |
| `paySchedule` | number |  |
| `plateNumber` | string |  |
| `propertyID` | object |  |
| `propertyName` | object |  |
| `purchasedDate` | string |  |
| `purchasedUserID` | number |  |
| `purchasedUserName` | string |  |
| `purchasePrice` | number |  |
| `renewalDate` | string |  |
| `requestedDate` | string |  |
| `requestedUserID` | number |  |
| `requestedUserName` | string |  |
| `routeID` | object |  |
| `routeName` | object |  |
| `serialNumber` | string |  |
| `trackerType` | string |  |
| `warrantyDays` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Equipments` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-equipments.md) for the provider-specific parameters and requirements.

