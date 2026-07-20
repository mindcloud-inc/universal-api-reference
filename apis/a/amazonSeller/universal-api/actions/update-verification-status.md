# Amazon Seller: Update Verification Status

Updates regulated order verification status in Amazon Seller.

```
PUT https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-verification-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-verification-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalReviewerId": "string",
  "orderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-verification-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalReviewerId": "string",
    "orderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalReviewerId` | string | yes | The identifier of the order's regulated information reviewer. |
| `orderId` | string | yes | The Amazon order identifier in 3-7-7 format. |
| `verificationDetails.prescriptionDetail` | object | no | Information about the prescription that is used to verify a regulated product. This must be provided once per order and reflect the seller’s own records. Only approved orders can have prescriptions. |
| `verificationDetails.prescriptionDetail.prescriptionId` | string | no | The identifier for the prescription used to verify the regulated product. |
| `rejectionReasonId` | string | no | The unique identifier of the rejection reason used for rejecting the order's regulated information. Only required if the new status is rejected. |
| `verificationDetails.prescriptionDetail.expirationDate` | string | no | The expiration date of the prescription used to verify the regulated product, in ISO 8601 date time format. |
| `status` | list | no | The verification status of the order. |
| `verificationDetails.prescriptionDetail.writtenQuantity` | number | no | The number of units in each fill as provided in the prescription. |
| `verificationDetails.prescriptionDetail.totalRefillsAuthorized` | number | no | The total number of refills written in the original prescription used to verify the regulated product. If a prescription originally had no refills, this value must be 0. |
| `verificationDetails` | object | no | Additional information related to the verification of a regulated order. |
| `verificationDetails.prescriptionDetail.refillsRemaining` | number | no | The number of refills remaining for the prescription used to verify the regulated product. If a prescription originally had 10 total refills, this value must be 10 for the first order, 9 for the second order, and 0 for the eleventh order. If a prescription originally had no refills, this value must be 0. |
| `verificationDetails.prescriptionDetail.clinicId` | string | no | The identifier for the clinic which provided the prescription used to verify the regulated product. |
| `verificationDetails.prescriptionDetail.usageInstructions` | string | no | The instructions for the prescription as provided by the approver of the regulated product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderId` | string | Amazon order identifier whose verification status was updated. |
| `status` | string | Updated verification status. |

## Native endpoint

Through the native Amazon Seller API, this operation is `PATCH orders/v0/orders/:orderId/regulatedInfo` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-verification-status.md) for the provider-specific parameters and requirements.

