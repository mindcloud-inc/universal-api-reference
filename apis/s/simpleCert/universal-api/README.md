# <img src="https://images.mindcloud.co/apps/icons/idd-oh-xn-z-d-1774551290463_1774551296537.png" alt="SimpleCert logo" width="28" height="28"> SimpleCert: Universal API

Create, send, and store certificates and recipients

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simpleCert/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://simplecert.net
- **Vendor API docs:** https://simplecert.readme.io/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Allowed Recipient Count](actions/get-allowed-recipient-count.md) | GET |  |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve API Key](actions/retrieve-api-key.md) | POST |  |

### Certificate

| Action | Method | Description |
| --- | --- | --- |
| [List Certificates](actions/list-certificates.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST |  |
| [List Project Recipients](actions/list-project-recipients.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

