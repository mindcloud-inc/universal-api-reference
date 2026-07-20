# <img src="https://images.mindcloud.co/apps/icons/images-24_1774884289236.png" alt="ClustDoc logo" width="28" height="28"> ClustDoc: Universal API

Manage Clustdoc teams, contacts, templates, applications, forms, portals, tags, and custom data fields through the Clustdoc REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clustDoc/latest
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clustdoc.com
- **Vendor API docs:** https://clustdoc.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | POST |  |
| [List Applications](actions/list-applications.md) | GET |  |
| [List Applications By Status](actions/list-applications-by-status.md) | GET |  |
| [List Applications By Template](actions/list-applications-by-template.md) | GET |  |
| [List On-Time Applications](actions/list-on-time-applications.md) | GET |  |
| [Search Applications](actions/search-applications.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Search Companies](actions/search-companies.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [List Active Contacts](actions/list-active-contacts.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Search Contacts](actions/search-contacts.md) | GET |  |
| [Search Contacts By Email](actions/search-contacts-by-email.md) | GET |  |

### Data Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Field](actions/create-data-field.md) | POST |  |
| [List Data Fields](actions/list-data-fields.md) | GET |  |
| [List Data Fields By Parent Type](actions/list-data-fields-by-parent-type.md) | GET |  |
| [List Text Data Fields](actions/list-text-data-fields.md) | GET |  |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST |  |
| [List Forms](actions/list-forms.md) | GET |  |
| [Search Forms By Title](actions/search-forms-by-title.md) | GET |  |

### Portal

| Action | Method | Description |
| --- | --- | --- |
| [Create Portal](actions/create-portal.md) | POST |  |
| [List Portals](actions/list-portals.md) | GET |  |
| [Search Portals By Title](actions/search-portals-by-title.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Search Tags](actions/search-tags.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Current Teams](actions/list-current-teams.md) | GET |  |
| [List Teams](actions/list-teams.md) | GET |  |
| [Search Teams](actions/search-teams.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [List Live Templates](actions/list-live-templates.md) | GET |  |
| [List Phone Collection Templates](actions/list-phone-collection-templates.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |
| [List Templates By Background](actions/list-templates-by-background.md) | GET |  |
| [List Templates By Language](actions/list-templates-by-language.md) | GET |  |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [List Uploads](actions/list-uploads.md) | GET |  |
| [List Uploads By Dossier Item](actions/list-uploads-by-dossier-item.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Owner Users](actions/list-owner-users.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Search Users](actions/search-users.md) | GET |  |

