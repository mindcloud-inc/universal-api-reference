# Send Template For Signing with BoloForms

Sends a BoloForms template for signing.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf-template-lambda`
- **Base URL:** `https://sapi.boloforms.com/signature`
- **Official documentation:** [Send Template For Signing](https://bolosign-developer-docs.readme.io/reference/post_pdf-template-lambda-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | body | `string` | yes | ID of the document template |
| `signingType` | body | `string` | yes | Must be PDF_TEMPLATE or FORM_TEMPLATE Accepted values: `0`, `1`. |
| `receiversList[]` | body | `array<object>` | yes | List of receivers who need to sign the document |
| `receiversList[].name` | body | `string` | yes | Name of the person |
| `receiversList[].email` | body | `string` | yes | Email of the person, it will send an email to the customer for signing |
| `receiversList[].roleTitle` | body | `string` | no | Must exactly match the role added while uploading PDF template in BoloSign dashboard |
| `receiversList[].subject` | body | `string` | no | Optional custom subject for this receiver |
| `receiversList[].message` | body | `string` | no | Optional custom message for this receiver |
| `mailData` | body | `object` | no | Global mail subject and message fallback values |
| `mailData.subject` | body | `string` | no | Global subject used when receiver-specific subject is not provided |
| `mailData.message` | body | `string` | no | Global message used when receiver-specific message is not provided |
| `customVariables[]` | body | `array<object>` | no | Optional custom variables to be replaced in the template |
| `customVariables[].varName` | body | `string` | yes | Variable name in square brackets, must match template exactly |
| `customVariables[].varValue` | body | `string` | yes | Value to be assigned to the variable |
| `pdfData` | body | `string` | no | Base64-encoded PDF data for PDF template sends |
