# Create Document with DocuPotion

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/create`
- **Base URL:** `https://api.docupotion.com`
- **Official documentation:** [Create Document](https://docupotion.com/api-docs#create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `list<string>` | yes | Choose the DocuPotion template to render. |
| `output` | body | `list<string>` | no | Accepted values: `Base64`, `URL`. |
| `expiration` | body | `number` | no | How many minutes the generated URL should remain valid when output is URL. |
| `format` | body | `list<string>` | no | Accepted values: `PDF`, `PNG`. |
| `data` | body | `object` | no | Dynamic data that matches the variables in your template. |
| `s3_bucket` | body | `boolean` | no | Upload the generated file to your connected S3 bucket instead of DocuPotion storage. |
| `s3_key` | body | `string` | no | Custom S3 object key without the file extension. |
