# Create PDF URL with DocuPotion

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/create`
- **Base URL:** `https://api.docupotion.com`
- **Official documentation:** [Create PDF URL](https://docupotion.com/api-docs#create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `list<string>` | yes | Choose the DocuPotion template to render. |
| `expiration` | body | `number` | no | How many minutes the generated URL should remain valid. |
| `data` | body | `object` | no | Dynamic data that matches the variables in your template. |
