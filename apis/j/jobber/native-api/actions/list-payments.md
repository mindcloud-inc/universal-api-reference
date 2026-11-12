# List Payments with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [List Payments](https://developer.getjobber.com/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `string` | no | Select the Jobber payment record fields to return. |
| `adjustmentType` | body | `list` | no | Only return payment records with the specified Jobber income adjustment type. Accepted values: `BAD_DEBT`, `CORRECTION`, `DEPOSIT`, `FAILED_ACH_PAYMENT`, `INITIAL_BALANCE`, `INVOICE`, `PAYMENT`, `REFUND`, `VOIDED`. |
| `entryDateAfter` | body | `date` | no | Only return payment records created after this entry date (ISO 8601). |
| `entryDateBefore` | body | `date` | no | Only return payment records created before this entry date (ISO 8601). |
