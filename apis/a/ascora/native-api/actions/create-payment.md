# Create Payment with Ascora

Creates a new payment in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Accounting/CreatePayment`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Payment](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=77)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | no | Free text comment associated with the Payment. |
| `invoiceNumber` | body | `string` | yes | Invoice Number in Ascora to which the Payment will be applied. |
| `paymentAmount` | body | `number` | yes | Amount of the Payment not including any credit card surcharge. |
| `paymentDate` | body | `date` | yes | Date associated with the Payment. |
| `paymentMethod` | body | `string` | yes | Name of the related Payment Method in Ascora. |
| `receiptNumber` | body | `string` | no | Transaction receipt number associated with the Payment. |
| `surchargeAmount` | body | `number` | no | Amount of any surcharge associated with processing the payment. |
