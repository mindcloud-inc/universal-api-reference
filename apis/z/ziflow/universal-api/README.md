# <img src="https://images.mindcloud.co/apps/icons/ziflow_1775243547404.png" alt="Ziflow logo" width="28" height="28"> Ziflow: Universal API

Ziflow is an online proofing platform. This app provides access to the Ziflow REST API for working with proofs, folders, users/contacts, integrations, and related resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ziflow/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ziflow.com/
- **Vendor API docs:** https://api-docs.ziflow.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Comment Label

| Action | Method | Description |
| --- | --- | --- |
| [Get Comment Label](actions/get-comment-label.md) | GET | Retrieves a comment label from Ziflow by ID. |
| [List Comment Labels](actions/list-comment-labels.md) | GET | Retrieves comment labels from your Ziflow account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Ziflow by ID or email. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Ziflow account. |

### Decision Checklist

| Action | Method | Description |
| --- | --- | --- |
| [List Decision Checklist](actions/list-decision-checklist.md) | GET | Retrieves decision checklist settings from Ziflow. |

### Decision Checklist Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Decision Checklist Option](actions/get-decision-checklist-option.md) | GET | Retrieves a decision checklist option from Ziflow. |

### Decision Reason

| Action | Method | Description |
| --- | --- | --- |
| [List Decision Reasons](actions/list-decision-reasons.md) | GET | Retrieves decision reasons settings from Ziflow. |

### Decision Reason Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Decision Reason Option](actions/get-decision-reason-option.md) | GET | Retrieves a decision reason option from Ziflow. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Generate Folder URL](actions/generate-folder-url.md) | GET | Retrieves a folder URL from Ziflow. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves subfolders in a Ziflow folder. |
| [List Root Folders](actions/list-root-folders.md) | GET | Retrieves root folders from your Ziflow account. |

### Intake Form

| Action | Method | Description |
| --- | --- | --- |
| [List Intake Forms](actions/list-intake-forms.md) | GET | Retrieves intake forms from your Ziflow account. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from your Ziflow account. |

### Integration Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Integration Connections](actions/list-integration-connections.md) | GET | Retrieves integration connections for a Ziflow app. |

### Integration Property Group

| Action | Method | Description |
| --- | --- | --- |
| [List Integration Property Groups](actions/list-integration-property-groups.md) | GET | Retrieves integration property groups from Ziflow. |

### Integration Property Group Property

| Action | Method | Description |
| --- | --- | --- |
| [List Integration Property Group Properties](actions/list-integration-property-group-properties.md) | GET | Retrieves integration property group properties from Ziflow. |

### Proof

| Action | Method | Description |
| --- | --- | --- |
| [Get Proof](actions/get-proof.md) | GET | Retrieves a proof from Ziflow by ID. |
| [Get Proof Reviewer URL](actions/get-proof-reviewer-url.md) | GET | Retrieves a reviewer's proof URL from Ziflow. |
| [List Proofs](actions/list-proofs.md) | GET | Retrieves proofs from your Ziflow account. |

### Proof Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Proof Activities](actions/list-proof-activities.md) | GET | Retrieves proof activities from Ziflow by proof ID. |

### Proof Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Proof Comment](actions/get-proof-comment.md) | GET | Retrieves a proof comment from Ziflow by ID. |
| [List Proof Comments](actions/list-proof-comments.md) | GET | Retrieves proof comments from Ziflow by proof ID. |

### Proof Custom Property Group

| Action | Method | Description |
| --- | --- | --- |
| [List Proof Custom Property Groups](actions/list-proof-custom-property-groups.md) | GET | Retrieves proof custom property groups from Ziflow. |

### Proof Email

| Action | Method | Description |
| --- | --- | --- |
| [List Proof Emails](actions/list-proof-emails.md) | GET | Retrieves proof emails from Ziflow by proof ID. |

### Proof Summary Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Export Proof Summary PDF](actions/export-proof-summary-pdf.md) | GET | Exports a proof summary to PDF from Ziflow. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Ziflow by ID or email. |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Ziflow account. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook subscriptions from your Ziflow account. |

### Workflow Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Template](actions/get-workflow-template.md) | GET | Retrieves a workflow template from Ziflow by ID. |
| [List Workflow Templates](actions/list-workflow-templates.md) | GET | Retrieves workflow templates from your Ziflow account. |

