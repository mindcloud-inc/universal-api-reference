# <img src="https://images.mindcloud.co/apps/icons/dropbox-sign_1773785756531.png" alt="Dropbox Sign logo" width="28" height="28"> Dropbox Sign: Universal API

Send, track, and manage signature requests and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dropboxSign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sign.dropbox.com
- **Vendor API docs:** https://developers.hellosign.com/api/api-reference-welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your Dropbox Sign account settings. |

### Api App

| Action | Method | Description |
| --- | --- | --- |
| [Get API App](actions/get-api-app.md) | GET | Retrieves an API app from Dropbox Sign by client ID. |
| [List API Apps](actions/list-api-apps.md) | GET | Retrieves API apps from Dropbox Sign. |

### Bulk Send Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Send Job](actions/get-bulk-send-job.md) | GET | Retrieves a bulk send job from Dropbox Sign by ID. |
| [List Bulk Send Jobs](actions/list-bulk-send-jobs.md) | GET | Retrieves bulk send jobs from Dropbox Sign. |

### Embedded Sign Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Embedded Sign URL](actions/get-embedded-sign-url.md) | GET | Retrieves an embedded signing URL from Dropbox Sign. |

### Embedded Template Edit Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Embedded Template Edit URL](actions/get-embedded-template-edit-url.md) | GET | Retrieves an embedded template edit URL from Dropbox Sign. |

### Signature Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Signature Request](actions/cancel-signature-request.md) | DELETE | Cancels a signature request in Dropbox Sign. |
| [Get Signature Request](actions/get-signature-request.md) | GET | Retrieves a signature request from Dropbox Sign by ID. |
| [List Signature Requests](actions/list-signature-requests.md) | GET | Retrieves signature requests from Dropbox Sign. |
| [Send Signature Request](actions/send-signature-request.md) | POST | Creates a signature request in Dropbox Sign. |
| [Send Signature Request Reminder](actions/send-signature-request-reminder.md) | PUT | Sends a signature request reminder in Dropbox Sign. |
| [Send Signature Request with Template](actions/send-signature-request-with-template.md) | POST | Creates a signature request from a template in Dropbox Sign. |

### Signature Request File

| Action | Method | Description |
| --- | --- | --- |
| [Get Signature Request Files](actions/get-signature-request-files.md) | GET | Retrieves signature request files from Dropbox Sign. |
| [Get Signature Request Files as Data URI](actions/get-signature-request-files-as-data-uri.md) | GET | Retrieves signature request files as data URIs from Dropbox Sign. |
| [Get Signature Request Files as File URL](actions/get-signature-request-files-as-file-url.md) | GET | Retrieves signature request files as file URLs from Dropbox Sign. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in Dropbox Sign. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Dropbox Sign by ID. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Dropbox Sign. |

### Template File

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Files](actions/get-template-files.md) | GET | Retrieves template files from Dropbox Sign. |
| [Get Template Files as Data URI](actions/get-template-files-as-data-uri.md) | GET | Retrieves template files as data URIs from Dropbox Sign. |
| [Get Template Files as File URL](actions/get-template-files-as-file-url.md) | GET | Retrieves template files as file URLs from Dropbox Sign. |

