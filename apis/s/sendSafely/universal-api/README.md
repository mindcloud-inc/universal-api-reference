# <img src="https://images.mindcloud.co/apps/icons/send-safely_1774042817307.png" alt="SendSafely logo" width="28" height="28"> SendSafely: Universal API

Secure file exchange and workspace management for SendSafely packages, recipients, directories, files, and contact groups.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendSafely/latest
- **Category:** Content & Files / Storage
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.sendsafely.com/
- **Vendor API docs:** https://rest-api-docs.sendsafely.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Credentials](actions/verify-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activity Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Activity Log](actions/get-workspace-activity-log.md) | GET |  |

### Collaborator

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborators](actions/list-collaborators.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Verify Credentials](actions/verify-credentials.md) | GET |  |

### Contact Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Group Member](actions/add-contact-group-member.md) | PUT |  |
| [Add Contact Group to Package](actions/add-contact-group-to-package.md) | PUT |  |
| [Create Contact Group](actions/create-contact-group.md) | POST |  |
| [Delete Contact Group](actions/delete-contact-group.md) | DELETE |  |
| [Delete Contact Group from Package](actions/delete-contact-group-from-package.md) | PUT |  |
| [Get Contact Group](actions/get-contact-group.md) | GET |  |
| [List User Contact Groups](actions/list-user-contact-groups.md) | GET |  |
| [Remove Contact Group Member](actions/remove-contact-group-member.md) | PUT |  |

### Directory

| Action | Method | Description |
| --- | --- | --- |
| [Create Subdirectory](actions/create-subdirectory.md) | POST |  |
| [Delete Directory](actions/delete-directory.md) | DELETE |  |
| [Get Directory](actions/get-directory.md) | GET |  |
| [Move Directory](actions/move-directory.md) | PUT |  |
| [Rename Directory](actions/rename-directory.md) | PUT |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Add File](actions/add-file.md) | POST |  |
| [Copy File To Workspace](actions/copy-file-to-workspace.md) | POST |  |
| [Delete Package File](actions/delete-package-file.md) | DELETE |  |
| [Get File Information](actions/get-file-information.md) | GET |  |
| [Move Workspace File](actions/move-workspace-file.md) | PUT |  |
| [Update File](actions/update-file.md) | PUT |  |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Create Package](actions/create-package.md) | POST |  |
| [Delete Package](actions/delete-package.md) | DELETE |  |
| [Finalize Package](actions/finalize-package.md) | PUT |  |
| [Get Package Information](actions/get-package-information.md) | GET |  |
| [List Archived Packages](actions/list-archived-packages.md) | GET |  |
| [List Received Packages](actions/list-received-packages.md) | GET |  |
| [List Sent Packages](actions/list-sent-packages.md) | GET |  |
| [List Workspace Packages](actions/list-workspace-packages.md) | GET |  |
| [Search Package](actions/search-package.md) | GET |  |
| [Update Package](actions/update-package.md) | PUT |  |

### Package Permission

| Action | Method | Description |
| --- | --- | --- |
| [List Package Permissions](actions/list-package-permissions.md) | GET |  |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Add Recipient](actions/add-recipient.md) | POST |  |
| [Add Recipients](actions/add-recipients.md) | POST |  |
| [Delete Recipients](actions/delete-recipients.md) | DELETE |  |
| [Get Recipient](actions/get-recipient.md) | GET |  |
| [Remove Recipient](actions/remove-recipient.md) | DELETE |  |
| [Update Recipient](actions/update-recipient.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET |  |

