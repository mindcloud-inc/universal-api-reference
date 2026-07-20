# <img src="https://images.mindcloud.co/apps/icons/digitink_1775491391234.png" alt="Digit.ink logo" width="28" height="28"> Digit.ink: Universal API

Issue and manage digital credentials, badges, batches, and stacks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/digitink/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.digit.ink/
- **Vendor API docs:** https://app.digit.ink/api/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Issuer Profile](actions/get-issuer-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-issuer-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch](actions/get-batch.md) | GET |  |
| [List Batches](actions/list-batches.md) | GET |  |

### Credential

| Action | Method | Description |
| --- | --- | --- |
| [Get Credential](actions/get-credential.md) | GET |  |
| [Get Credential Stack](actions/get-credential-stack.md) | GET |  |
| [Issue Credentials](actions/issue-credentials.md) | POST |  |
| [List Credentials](actions/list-credentials.md) | GET |  |

### Issuer

| Action | Method | Description |
| --- | --- | --- |
| [Get Issuer Profile](actions/get-issuer-profile.md) | GET |  |

### Stack

| Action | Method | Description |
| --- | --- | --- |
| [Add Batch To Stack](actions/add-batch-to-stack.md) | PUT |  |
| [Create Stack](actions/create-stack.md) | POST |  |
| [Delete Stacks](actions/delete-stacks.md) | DELETE |  |
| [Get Stack](actions/get-stack.md) | GET |  |
| [List Stacks](actions/list-stacks.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

