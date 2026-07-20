# Get Package Shipping Document with TikTok Shop

For orders shipped by TikTok Shop, this API retrieves the URL of shipping documents (shipping label and packing slip) for a package specified by the package ID.

## Endpoint

- **Method:** `GET`
- **Path:** `fulfillment/202309/packages/:packageId/shipping_documents`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Package Shipping Document](https://partner.tiktokshop.com/docv2/page/get-package-shipping-document-202309)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `string` | yes | A TikTok Shop package ID. |
| `shop_cipher` | query | `list<string>` | no | — |
| `document_type` | query | `list<string>` | yes | Available document types:  - `SHIPPING_LABEL`: Returns the shipping label in PDF format by default. - `PACKING_SLIP`: Returns the packing slip in PDF format by default. - `SHIPPING_LABEL_AND_PACKING_SLIP`: Returns both the shipping label and the packing slip for the package, both in PDF format by default.               - `SHIPPING_LABEL_PICTURE`: Returns the shipping label in PNG format.  - `HAZMAT_LABEL`: Returns the hazmat label in PDF format by default. You must only use this value when there are hazmat items in the package. When you use this value, `document_size` is fixed to `A4`, and you don't need to specify it. - `INVOICE_LABEL`: For Brazil market only, document_size is fixed to `A6`, and you don't need to specify document_size. Returns the invoice label in PDF format by default. |
| `document_size` | query | `list<string>` | no | Specify the size of the document to obtain. This parameter is only applicable to shipping labels, picking slips, and packing slips that are in the PDF format. It is not applicable for hazmat labels as these are fixed to `A4`.  If you specify `SHIPPING_LABEL_PICTURE` for the `document_type`, any value specified will be ignored.  Possible values:  - `A6` (Default) - `A5` |
| `document_format` | query | `list<string>` | no | The format of the shipping document. Possible values:  - `PDF` (Default) - `ZPL` (Only for BR market)  **Note**: Not applicable for `SHIPPING_LABEL_PICTURE` document type. |
