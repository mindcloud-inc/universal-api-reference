# <img src="https://images.mindcloud.co/apps/icons/images_1773437454421.png" alt="Certifier logo" width="28" height="28"> Certifier: Universal API

Create, issue, and manage digital certificates and badges

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/certifier/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://certifier.io
- **Vendor API docs:** https://developers.certifier.io/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credential](actions/get-credential.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-credential?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Attributes](actions/list-attributes.md) | GET | Retrieves all available attributes from Certifier. |

### Credential

| Action | Method | Description |
| --- | --- | --- |
| [Create Credential](actions/create-credential.md) | POST | Creates a new credential in Certifier. |
| [Create, Issue, and Send Credential](actions/create-issue-and-send-credential.md) | POST | Creates, issues, and sends a credential in Certifier. |
| [Delete Credential](actions/delete-credential.md) | DELETE | Deletes an existing credential from Certifier. |
| [Get Credential](actions/get-credential.md) | GET | Retrieves detailed credential information from Certifier. |
| [Issue Credential](actions/issue-credential.md) | PUT | Issues an existing credential in Certifier. |
| [List Credentials](actions/list-credentials.md) | GET | Retrieves all available credentials from Certifier. |
| [Schedule Credential Issuance](actions/schedule-credential-issuance.md) | PUT | Schedules future credential issuance in Certifier. |
| [Search Credentials](actions/search-credentials.md) | GET | Finds credentials in Certifier by structured search criteria. |
| [Send Credential](actions/send-credential.md) | PUT | Sends an existing credential from Certifier. |
| [Update Credential](actions/update-credential.md) | PUT | Updates an existing credential in Certifier. |

### Credential Interaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Credential Interaction](actions/create-credential-interaction.md) | POST | Creates a credential interaction in Certifier. |
| [List Credential Interactions](actions/list-credential-interactions.md) | GET | Retrieves all credential interactions from Certifier. |

### Design

| Action | Method | Description |
| --- | --- | --- |
| [Get Design](actions/get-design.md) | GET | Retrieves detailed design information from Certifier. |
| [List Credential Designs](actions/list-credential-designs.md) | GET | Retrieves all credential-specific designs from Certifier. |
| [List Designs](actions/list-designs.md) | GET | Retrieves all available designs from Certifier. |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves all email templates from Certifier. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Certifier. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Certifier. |
| [Get Group](actions/get-group.md) | GET | Retrieves detailed group information from Certifier. |
| [List Groups](actions/list-groups.md) | GET | Retrieves all available groups from Certifier. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Certifier. |

