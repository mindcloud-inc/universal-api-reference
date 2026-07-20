# Update Verification Status with Amazon Seller

Updates regulated order verification status in Amazon Seller.

## Endpoint

- **Method:** `PATCH`
- **Path:** `orders/v0/orders/:orderId/regulatedInfo`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Update Verification Status](https://developer-docs.amazon.com/sp-api/reference/updateverificationstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalReviewerId` | body | `string` | yes | The identifier of the order's regulated information reviewer. |
| `orderId` | path | `string` | yes | The Amazon order identifier in 3-7-7 format. |
| `verificationDetails.prescriptionDetail` | body | `object` | no | Information about the prescription that is used to verify a regulated product. This must be provided once per order and reflect the seller’s own records. Only approved orders can have prescriptions. |
| `verificationDetails.prescriptionDetail.prescriptionId` | body | `string` | no | The identifier for the prescription used to verify the regulated product. |
| `rejectionReasonId` | body | `string` | no | The unique identifier of the rejection reason used for rejecting the order's regulated information. Only required if the new status is rejected. |
| `verificationDetails.prescriptionDetail.expirationDate` | body | `string` | no | The expiration date of the prescription used to verify the regulated product, in ISO 8601 date time format. |
| `status` | body | `list` | no | The verification status of the order. |
| `verificationDetails.prescriptionDetail.writtenQuantity` | body | `number` | no | The number of units in each fill as provided in the prescription. |
| `verificationDetails.prescriptionDetail.totalRefillsAuthorized` | body | `number` | no | The total number of refills written in the original prescription used to verify the regulated product. If a prescription originally had no refills, this value must be 0. |
| `verificationDetails` | body | `object` | no | Additional information related to the verification of a regulated order. |
| `verificationDetails.prescriptionDetail.refillsRemaining` | body | `number` | no | The number of refills remaining for the prescription used to verify the regulated product. If a prescription originally had 10 total refills, this value must be 10 for the first order, 9 for the second order, and 0 for the eleventh order. If a prescription originally had no refills, this value must be 0. |
| `verificationDetails.prescriptionDetail.clinicId` | body | `string` | no | The identifier for the clinic which provided the prescription used to verify the regulated product. |
| `verificationDetails.prescriptionDetail.usageInstructions` | body | `string` | no | The instructions for the prescription as provided by the approver of the regulated product. |
