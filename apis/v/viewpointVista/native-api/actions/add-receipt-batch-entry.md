# Add Receipt Batch Entry with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ar/2/data/batch_entries/actions/add_receipt`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add Receipt Batch Entry](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatch_entriesactionsadd_receipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Key to ar/batches(Co, Mth, BatchId). |
| `Mth` | body | `string` | yes | Key to ar/batches(Co, Mth, BatchId). Format: YYYY-MM-01. |
| `BatchId` | body | `number` | yes | Key to ar/batches(Co, Mth, BatchId). |
| `Customer` | body | `number` | yes | Key to ar/customers(CustGroup, Customer). CustGroup is defaulted based on Co. |
| `TransDate` | body | `string` | no | Transaction date. Format: YYYY-MM-DD. Optional; defaults to today. |
| `CheckNo` | body | `string` | no | Check number. Optional. |
| `CheckDate` | body | `string` | no | Check date. Format: YYYY-MM-DD. Optional. |
| `CreditAmt` | body | `string` | yes | Check amount. |
| `CMCo` | body | `number` | no | CM company. Optional; defaults based on AR company settings. |
| `CMAcct` | body | `number` | no | CM account. Optional; defaults based on AR company settings. |
| `CMDeposit` | body | `string` | yes | Deposit number. |
| `Notes` | body | `string` | no | Optional notes. |
| `__custom_fields` | body | `object` | no | User-defined values to set on the batch transaction header. |
| `miscDistributions[]` | body | `array<object>` | no | Optional misc distribution rows for the receipt. |
| `LineItems[]` | body | `array<object>` | no | Optional receipt application rows. |
| `MiscDistCode` | body | `string` | no | Misc distribution code. |
| `DistDate` | body | `date` | no | Distribution date. Format: YYYY-MM-DD. |
| `Description` | body | `string` | no | Optional misc distribution description. |
| `Amount` | body | `string` | no | Misc distribution amount. |
| `__custom_fields` | body | `object` | no | User-defined values to set on the misc distribution. |
| `LineItems[].ARLine` | body | `number` | no | Optional line number. If omitted, Vista defaults the next ARLine number. |
| `LineItems[].LineType` | body | `list<string>` | no | C applies payment to an invoice line. A applies funds on account. Accepted values: `A`, `C`. |
| `LineItems[].ApplyMth` | body | `date` | no | Reference month for the transaction line being paid or for previously saved on-account funds. Format: YYYY-MM-01. |
| `LineItems[].ApplyTrans` | body | `number` | no | Reference transaction being paid or prior on-account receipt transaction. |
| `LineItems[].ApplyLine` | body | `number` | no | Reference transaction line being paid or prior on-account receipt line. |
| `LineItems[].Amount` | body | `string` | no | Amount applied for this line item or on-account adjustment amount. |
| `LineItems[].DiscTaken` | body | `string` | no | Optional discount amount to take on this line item. |
| `LineItems[].TaxAmount` | body | `string` | no | Optional tax amount applied to an invoice line item. |
| `LineItems[].Retainage` | body | `string` | no | Optional retainage amount applied to an invoice line item. |
| `LineItems[].Notes` | body | `string` | no | Optional line-item notes. |
| `LineItems[].__custom_fields` | body | `object` | no | User-defined values to set on the receipt line item. |
| `LineItems[].RecType` | body | `number` | no | Receivable type for on-account line items. Optional. |
| `LineItems[].Description` | body | `string` | no | Optional description for on-account line items. |
| `LineItems[].tax` | body | `object` | no | Optional tax details for on-account line items. |
| `LineItems[].tax.TaxCode` | body | `string` | no | Optional tax code for on-account line items. |
| `LineItems[].tax.TaxBasis` | body | `string` | no | Optional tax basis amount for on-account line items. |
| `LineItems[].tax.TaxAmount` | body | `string` | no | Optional tax amount for on-account line items. |
