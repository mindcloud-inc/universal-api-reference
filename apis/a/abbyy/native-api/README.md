# Abbyy: Native API Reference

A consolidated summary of Abbyy's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference
- **API base URL:** `https://cloud-westus.ocrsdk.com`

## Authentication

### Basic Authentication

Authenticate ABBYY Cloud OCR SDK requests with your Application ID and Application Password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.abbyy.com/hc/en-us/articles/360017326739-Authentication)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Task](actions/delete-task.md) | `POST /v2/deleteTask` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference) |
| [Get Task Status](actions/get-task-status.md) | `GET /v2/getTaskStatus` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference) |
| [List Finished Tasks](actions/list-finished-tasks.md) | `GET /v2/listFinishedTasks` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269600-listFinishedTasks-Method) |
| [List Tasks](actions/list-tasks.md) | `GET /v2/listTasks` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference) |
| [Process Barcode Field](actions/process-barcode-field.md) | `POST /v2/processBarcodeField` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference) |
| [Process Business Card](actions/process-business-card.md) | `POST /v2/processBusinessCard` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269740-processBusinessCard-Method) |
| [Process Checkmark Field](actions/process-checkmark-field.md) | `POST /v2/processCheckmarkField` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference) |
| [Process Document](actions/process-document.md) | `POST /v2/processDocument` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference) |
| [Process Fields](actions/process-fields.md) | `POST /v2/processFields` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269520-processFields-Method) |
| [Process Image](actions/process-image.md) | `POST /v2/processImage` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference) |
| [Process MRZ](actions/process-mrz.md) | `POST /v2/processMRZ` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference) |
| [Process Text Field](actions/process-text-field.md) | `POST /v2/processTextField` | [docs](https://support.abbyy.com/hc/en-us/articles/360017326359-How-to-recognize-text-fields) |
| [Submit Image](actions/submit-image.md) | `POST /v2/submitImage` | [docs](https://support.abbyy.com/hc/en-us/articles/360017269700-submitImage-Method) |
