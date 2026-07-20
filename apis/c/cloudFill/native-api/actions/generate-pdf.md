# Generate PDF with CloudFill

Generates a PDF from a CloudFill template.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pdf/{pdfKey}/generate`
- **Base URL:** `https://api.cloudfill.io`
- **Official documentation:** [Generate PDF](https://api.swaggerhub.com/apis/hpoul/CloudFill/1.3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdfKey` | path | `string` | yes | CloudFill PDF template key. |
| `variables` | body | `object` | no | Map variable keys to replacement text values. |
| `images` | body | `object` | no | Map image field keys to public image URL objects. |
| `flatten` | body | `list<string>` | no | Whether generated PDF form fields should be flattened. Accepted values: `all`, `none`. |
| `protectionPolicy` | body | `object` | no | Optional PDF protection policy settings. |
