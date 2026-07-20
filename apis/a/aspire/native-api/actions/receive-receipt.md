# Receive Receipt with Aspire

Marks an existing Aspire receipt as received. This action accepts the receipt identifier only and does not perform receipt-level edits. It cannot set or change invoice metadata, notes, extra costs or freight, receipt items, received date, or any other receipt field. If the user wants to record vendor invoice number or vendor invoice date around the same workflow, use approveReceipt because approveReceipt is the only post-create path for those two fields. For any other requested change to an existing receipt, explain that Aspire has no updateReceipt or patch action and the receipt must be recreated with the correct values.

## Endpoint

- **Method:** `POST`
- **Path:** `Receipts/Receive`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Receive Receipt](https://guide.youraspire.com/apidocs/receiptsreceive)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ReceiptID` | body | `list<number>` | no |
