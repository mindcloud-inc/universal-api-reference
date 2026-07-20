# Create Document to Connected S3 with DocuPotion

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/create`
- **Base URL:** `https://api.docupotion.com`
- **Official documentation:** [Create Document to Connected S3](https://docupotion.com/api-docs#create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `list<string>` | yes | Choose the DocuPotion template to render. |
| `expiration` | body | `number` | no | How many minutes the generated S3 URL should remain valid. |
| `format` | body | `list<string>` | no | Accepted values: `PDF`, `PNG`. |
| `data` | body | `object` | no | Dynamic data that matches the variables in your template. |
| `s3_key` | body | `string` | no | Custom S3 object key without the file extension. |
