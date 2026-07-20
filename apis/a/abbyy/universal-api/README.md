# <img src="https://images.mindcloud.co/apps/icons/yeii56tk-rbkxl-hlz9oll-rgb-logo-abbyy_1780947749526.png" alt="Abbyy logo" width="28" height="28"> Abbyy: Universal API

Use ABBYY Cloud OCR SDK to submit OCR jobs, inspect processing tasks, and retrieve recognition results from ABBYY's cloud OCR API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/abbyy/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.abbyy.com/
- **Vendor API docs:** https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Ocr Task

| Action | Method | Description |
| --- | --- | --- |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing OCR task from ABBYY Cloud OCR SDK. |
| [Get Task Status](actions/get-task-status.md) | GET | Retrieves the current status of an ABBYY OCR task. |
| [List Finished Tasks](actions/list-finished-tasks.md) | GET | Retrieves finished OCR tasks from ABBYY Cloud OCR SDK. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves OCR tasks from ABBYY Cloud OCR SDK. |
| [Process Barcode Field](actions/process-barcode-field.md) | POST | Creates an OCR task for a barcode field in ABBYY. |
| [Process Business Card](actions/process-business-card.md) | POST | Creates a business card OCR task in ABBYY Cloud OCR SDK. |
| [Process Checkmark Field](actions/process-checkmark-field.md) | POST | Creates an OCR task for a checkmark field in ABBYY. |
| [Process Document](actions/process-document.md) | PUT | Processes submitted images as one document in ABBYY Cloud OCR SDK. |
| [Process Fields](actions/process-fields.md) | PUT | Processes multiple fields in ABBYY Cloud OCR SDK. |
| [Process Image](actions/process-image.md) | POST | Creates an OCR task from an uploaded image in ABBYY. |
| [Process MRZ](actions/process-mrz.md) | POST | Creates an OCR task for MRZ data in ABBYY. |
| [Process Text Field](actions/process-text-field.md) | POST | Creates an OCR task for a text field in ABBYY. |
| [Submit Image](actions/submit-image.md) | POST | Uploads an image to an ABBYY OCR task, creating one if needed. |

