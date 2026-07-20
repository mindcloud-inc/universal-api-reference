# Create PDF Base64 with DocuPotion

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/create`
- **Base URL:** `https://api.docupotion.com`
- **Official documentation:** [Create PDF Base64](https://docupotion.com/api-docs#create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `list<string>` | yes | Choose the DocuPotion template to render. |
| `data` | body | `object` | no | Dynamic data that matches the variables in your template. |
