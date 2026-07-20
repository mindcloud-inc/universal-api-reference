# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-23-at-17_1774296598367.png" alt="Sign.Plus logo" width="28" height="28"> Sign.Plus: Universal API

Send, sign, and manage envelopes, templates, and signed documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/signPlus/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sign.plus
- **Vendor API docs:** https://apidoc.sign.plus/get-started/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Envelopes](actions/list-envelopes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelopes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Add Envelope Annotation](actions/add-envelope-annotation.md) | POST |  |
| [List Envelope Annotations](actions/list-envelope-annotations.md) | GET |  |

### Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Get Envelope Certificate](actions/get-envelope-certificate.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Add Envelope Document](actions/add-envelope-document.md) | POST |  |
| [Get Envelope Document](actions/get-envelope-document.md) | GET |  |
| [List Envelope Documents](actions/list-envelope-documents.md) | GET |  |

### Envelope

| Action | Method | Description |
| --- | --- | --- |
| [Add Envelope Signing Steps](actions/add-envelope-signing-steps.md) | PUT |  |
| [Create Envelope](actions/create-envelope.md) | POST |  |
| [Create Envelope from Template](actions/create-envelope-from-template.md) | POST |  |
| [Duplicate Envelope](actions/duplicate-envelope.md) | POST |  |
| [Get Envelope](actions/get-envelope.md) | GET |  |
| [List Envelopes](actions/list-envelopes.md) | GET |  |
| [Rename Envelope](actions/rename-envelope.md) | PUT |  |
| [Send Envelope](actions/send-envelope.md) | PUT |  |
| [Set Envelope Comment](actions/set-envelope-comment.md) | PUT |  |
| [Set Envelope Dynamic Fields](actions/set-envelope-dynamic-fields.md) | PUT |  |
| [Set Envelope Expiration Date](actions/set-envelope-expiration-date.md) | PUT |  |
| [Set Envelope Legality Level](actions/set-envelope-legality-level.md) | PUT |  |
| [Set Envelope Notification](actions/set-envelope-notification.md) | PUT |  |
| [Void Envelope](actions/void-envelope.md) | PUT |  |

### Signed Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Signed Document](actions/get-signed-document.md) | GET |  |
| [List Signed Documents](actions/list-signed-documents.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [Get Template](actions/get-template.md) | GET |  |

