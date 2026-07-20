# <img src="https://images.mindcloud.co/apps/icons/favicon-28_1777490809772.png" alt="iLoveSign logo" width="28" height="28"> iLoveSign: Universal API

iLoveSign lets you create, send, and manage electronic signature requests through the iLoveAPI signature REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iLoveSign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ilovesign.com/
- **Vendor API docs:** https://www.iloveapi.com/docs/signature-guides

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate Project](actions/authenticate-project.md) | POST |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Audit](actions/download-audit.md) | GET |  |
| [Download Original Files](actions/download-original-files.md) | GET |  |
| [Download Signed Files](actions/download-signed-files.md) | GET |  |
| [Remove Uploaded File](actions/remove-uploaded-file.md) | DELETE |  |
| [Upload File From URL](actions/upload-file-from-url.md) | POST |  |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Signature Status](actions/get-signature-status.md) | GET |  |
| [Increase Expiration Days](actions/increase-expiration-days.md) | PUT |  |
| [List Signatures](actions/list-signatures.md) | GET |  |
| [Send Reminder](actions/send-reminder.md) | PUT |  |
| [Void Signature](actions/void-signature.md) | PUT |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Connect Task](actions/connect-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Start Sign Task](actions/start-sign-task.md) | POST |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Fix Receiver Email](actions/fix-receiver-email.md) | PUT |  |
| [Fix Signer Phone](actions/fix-signer-phone.md) | PUT |  |
| [Get Receiver Info](actions/get-receiver-info.md) | GET |  |

