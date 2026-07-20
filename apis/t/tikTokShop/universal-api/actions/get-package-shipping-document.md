# TikTok Shop: Get Package Shipping Document

For orders shipped by TikTok Shop, this API retrieves the URL of shipping documents (shipping label and packing slip) for a package specified by the package ID.

```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-shipping-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-shipping-document?connectionId=$CONNECTION_ID&packageId=string&documentType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "string",
  "documentType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-shipping-document?${params}`, {
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
| `packageId` | string | yes | A TikTok Shop package ID. |
| `shop_cipher` | list<string> | no |  |
| `documentType` | list<string> | yes | Available document types: - `SHIPPING_LABEL`: Returns the shipping label in PDF format by default. - `PACKING_SLIP`: Returns the packing slip in PDF format by default. - `SHIPPING_LABEL_AND_PACKING_SLIP`: Returns both the shipping label and the packing slip for the package, both in PDF format by default. - `SHIPPING_LABEL_PICTURE`: Returns the shipping label in PNG format. - `HAZMAT_LABEL`: Returns the hazmat label in PDF format by default. You must only use this value when there are hazmat items in the package. When you use this value, `document_size` is fixed to `A4`, and you don't need to specify it. - `INVOICE_LABEL`: For Brazil market only, document_size is fixed to `A6`, and you don't need to specify document_size. Returns the invoice label in PDF format by default. |
| `documentSize` | list<string> | no | Specify the size of the document to obtain. This parameter is only applicable to shipping labels, picking slips, and packing slips that are in the PDF format. It is not applicable for hazmat labels as these are fixed to `A4`. If you specify `SHIPPING_LABEL_PICTURE` for the `document_type`, any value specified will be ignored. Possible values: - `A6` (Default) - `A5` |
| `documentFormat` | list<string> | no | The format of the shipping document. Possible values: - `PDF` (Default) - `ZPL` (Only for BR market) **Note**: Not applicable for `SHIPPING_LABEL_PICTURE` document type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `GET fulfillment/202309/packages/:packageId/shipping_documents` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-shipping-document.md) for the provider-specific parameters and requirements.

