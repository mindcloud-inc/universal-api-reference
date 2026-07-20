# <img src="https://images.mindcloud.co/apps/icons/images-36_1775044587815.png" alt="Qntrl logo" width="28" height="28"> Qntrl: Universal API

Qntrl: Manage cards, forms, blueprints, and workflow activity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qntrl/latest
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/qntrl/
- **Vendor API docs:** https://core.qntrl.com/apidoc.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization Details](actions/get-organization-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-organization-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Card Activities](actions/list-card-activities.md) | GET | Retrieves card activities from Qntrl. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment Details](actions/get-attachment-details.md) | GET | Retrieves attachment details from Qntrl. |
| [List Card Attachments](actions/list-card-attachments.md) | GET | Retrieves card attachments from Qntrl. |

### Blueprint

| Action | Method | Description |
| --- | --- | --- |
| [Get Blueprint Details](actions/get-blueprint-details.md) | GET | Retrieves blueprint details from Qntrl. |
| [List Active Blueprints](actions/list-active-blueprints.md) | GET | Retrieves active blueprints from Qntrl. |
| [List Blueprints](actions/list-blueprints.md) | GET | Retrieves blueprints from Qntrl. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Get Card Details](actions/get-card-details.md) | GET | Retrieves card details from Qntrl. |
| [List Cards](actions/list-cards.md) | GET | Retrieves a list of cards from Qntrl. |
| [List Deleted Cards](actions/list-deleted-cards.md) | GET | Retrieves deleted cards from Qntrl. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Card Comment Details](actions/get-card-comment-details.md) | GET | Retrieves card comment details from Qntrl. |
| [List Card Comments](actions/list-card-comments.md) | GET | Retrieves card comments from Qntrl. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Field Details](actions/get-custom-field-details.md) | GET | Retrieves custom field details from Qntrl. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from Qntrl. |

### Custom View

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom View Details](actions/get-custom-view-details.md) | GET | Retrieves custom view details from Qntrl. |
| [List Custom Views](actions/list-custom-views.md) | GET | Retrieves custom views from Qntrl. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Details](actions/get-form-details.md) | GET | Retrieves form details from Qntrl. |
| [List Forms](actions/list-forms.md) | GET | Retrieves a list of forms from Qntrl. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from Qntrl. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves organization details from Qntrl. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile Details](actions/get-profile-details.md) | GET | Retrieves profile details from Qntrl. |
| [List Profile Permissions](actions/list-profile-permissions.md) | GET | Retrieves profile permissions from Qntrl. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves profiles from Qntrl. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Report Details](actions/get-report-details.md) | GET | Retrieves report details from Qntrl. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from Qntrl. |

### Report Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Report Folder Details](actions/get-report-folder-details.md) | GET | Retrieves report folder details from Qntrl. |
| [List Report Folders](actions/list-report-folders.md) | GET | Retrieves report folders from Qntrl. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Get Role Details](actions/get-role-details.md) | GET | Retrieves role details from Qntrl. |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from Qntrl. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Row Details](actions/get-row-details.md) | GET | Retrieves row details from a Qntrl table. |
| [List Rows](actions/list-rows.md) | GET | Retrieves rows from a Qntrl table. |

### Stage

| Action | Method | Description |
| --- | --- | --- |
| [Get Stage Details](actions/get-stage-details.md) | GET | Retrieves stage details from Qntrl. |
| [List Stages](actions/list-stages.md) | GET | Retrieves a list of stages from Qntrl. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Details](actions/get-table-details.md) | GET | Retrieves table details from Qntrl. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from Qntrl. |

### Transition

| Action | Method | Description |
| --- | --- | --- |
| [List Next Card Transitions](actions/list-next-card-transitions.md) | GET | Retrieves next card transitions from Qntrl. |

### Transition Rule

| Action | Method | Description |
| --- | --- | --- |
| [Get Transition Rule](actions/get-transition-rule.md) | GET | Retrieves a transition rule from Qntrl. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get My User Details](actions/get-my-user-details.md) | GET | Retrieves your user details from Qntrl. |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves user details from Qntrl. |
| [List User Dropdown Values](actions/list-user-dropdown-values.md) | GET | Retrieves user dropdown values from Qntrl. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Qntrl. |

### User Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get User Activity](actions/get-user-activity.md) | GET | Retrieves user activity from Qntrl. |

### User Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Users](actions/export-users.md) | GET | Retrieves an exported user list from Qntrl. |

