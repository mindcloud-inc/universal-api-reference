# Add Restrictions with PDF Blocks

Updates a PDF document with restrictions in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/add_restrictions`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Add Restrictions](https://www.pdfblocks.com/docs/api/add-restrictions-to-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The input PDF document. |
| `owner_password` | body | `string` | yes | The password required to open and change permissions of the PDF document. |
| `user_password` | body | `string` | no | The password required to open the PDF document. |
| `encryption_algorithm` | body | `string` | no | The algorithm used to encrypt the PDF document. |
| `allow_copy_content` | body | `boolean` | no | If false, the user cannot copy text and images to the clipboard. |
| `allow_change_content` | body | `boolean` | no | If false, the user cannot change the content of the document. |
| `allow_print` | body | `boolean` | no | If false, the user cannot print the document. |
| `allow_print_high_resolution` | body | `boolean` | no | If false, the user cannot print the document in high resolution. |
| `allow_comment_and_fill_form` | body | `boolean` | no | If false, the user cannot add, edit, or modify annotations or fill form fields. |
| `allow_fill_form` | body | `boolean` | no | If false, the user cannot fill form fields. |
| `allow_assemble_document` | body | `boolean` | no | If false, the user cannot assemble or manipulate the document. |
| `allow_accessibility` | body | `boolean` | no | If false, accessibility programs cannot read the text or images of the document. |
