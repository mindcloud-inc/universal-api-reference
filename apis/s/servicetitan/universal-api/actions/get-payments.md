# ServiceTitan: Get Payments

Gets a paginated list of payments

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payments?${params}`, {
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
| `modifiedOnOrAfter` | string | no |  |
| `statuses` | string | no |  |
| `totalLess` | number | no |  |
| `totalGreater` | number | no |  |
| `ids` | string | no |  |
| `createdBefore` | string | no | Return items created before certain date/time (in UTC) |
| `createdOnOrAfter` | string | no | Return items created on or after certain date/time (in UTC) |
| `sort` | string | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "appliedTo": [
        {
          "appliedAmount": "string",
          "appliedBy": "string",
          "appliedId": 1,
          "appliedOn": "string",
          "appliedTo": 1,
          "appliedToReferenceNumber": "string"
        }
      ],
      "authCode": "string",
      "batch": {
        "id": 1,
        "name": "Ava Chen",
        "number": "string"
      },
      "businessUnit": {
        "id": 1,
        "name": "Ava Chen"
      },
      "checkNumber": "string",
      "createdBy": "string",
      "createdOn": "string",
      "customer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "customFields": {},
      "date": "string",
      "deposit": {
        "id": 1,
        "name": "Ava Chen"
      },
      "generalLedgerAccount": {
        "detailType": "string",
        "id": 1,
        "name": "Ava Chen",
        "number": "string",
        "type": "string"
      },
      "id": 1,
      "memo": "string",
      "modifiedOn": "string",
      "referenceNumber": "string",
      "refundedPaymentId": {},
      "syncStatus": "string",
      "total": "string",
      "type": "string",
      "typeId": "string",
      "unappliedAmount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `appliedTo[].appliedAmount` | string |  |
| `appliedTo[].appliedBy` | string |  |
| `appliedTo[].appliedId` | number |  |
| `appliedTo[].appliedOn` | string |  |
| `appliedTo[].appliedTo` | number |  |
| `appliedTo[].appliedToReferenceNumber` | string |  |
| `authCode` | string |  |
| `batch.id` | number |  |
| `batch.name` | string |  |
| `batch.number` | string |  |
| `businessUnit.id` | number |  |
| `businessUnit.name` | string |  |
| `checkNumber` | string |  |
| `createdBy` | string |  |
| `createdOn` | string |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customFields` | object |  |
| `date` | string |  |
| `deposit.id` | number |  |
| `deposit.name` | string |  |
| `generalLedgerAccount.detailType` | string |  |
| `generalLedgerAccount.id` | number |  |
| `generalLedgerAccount.name` | string |  |
| `generalLedgerAccount.number` | string |  |
| `generalLedgerAccount.type` | string |  |
| `id` | number |  |
| `memo` | string |  |
| `modifiedOn` | string |  |
| `referenceNumber` | string |  |
| `refundedPaymentId` | object |  |
| `syncStatus` | string |  |
| `total` | string |  |
| `type` | string |  |
| `typeId` | string |  |
| `unappliedAmount` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET accounting/v2/tenant/{{credentials.tenant}}/payments` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-payments.md) for the provider-specific parameters and requirements.

