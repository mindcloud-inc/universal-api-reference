# <img src="https://images.mindcloud.co/apps/icons/harvestr_1774534460343.png" alt="Harvestr.io logo" width="28" height="28"> Harvestr.io: Universal API

Harvestr is product management software for high-growth B2B SaaS teams, with APIs for users, companies, discoveries, feedback, messages, attributes, and related resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/harvestr/latest
- **Category:** Productivity / Project Management
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://harvestr.io
- **Vendor API docs:** https://developers.harvestr.io/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Company Attributes](actions/list-company-attributes.md) | GET |  |
| [List User Attributes](actions/list-user-attributes.md) | GET |  |

### Attribute Value

| Action | Method | Description |
| --- | --- | --- |
| [List Company Attribute Values](actions/list-company-attribute-values.md) | GET |  |
| [List User Attribute Values](actions/list-user-attribute-values.md) | GET |  |
| [Update Company Attribute Values](actions/update-company-attribute-values.md) | PUT |  |
| [Update User Attribute Values](actions/update-user-attribute-values.md) | PUT |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Retrieve Company](actions/retrieve-company.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Component

| Action | Method | Description |
| --- | --- | --- |
| [List Components](actions/list-components.md) | GET |  |
| [Retrieve Component](actions/retrieve-component.md) | GET |  |

### Custom Inbox

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Inboxes](actions/list-custom-inboxes.md) | GET |  |

### Discovery

| Action | Method | Description |
| --- | --- | --- |
| [List Discoveries](actions/list-discoveries.md) | GET |  |
| [Retrieve Discovery](actions/retrieve-discovery.md) | GET |  |
| [Update Discovery](actions/update-discovery.md) | PUT |  |

### Discovery State

| Action | Method | Description |
| --- | --- | --- |
| [Get Discovery State](actions/get-discovery-state.md) | GET |  |
| [List Discovery States](actions/list-discovery-states.md) | GET |  |
| [Retrieve Discovery State](actions/retrieve-discovery-state.md) | GET |  |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | POST |  |
| [List Discovery Feedback](actions/list-discovery-feedback.md) | GET |  |
| [List Feedback](actions/list-feedback.md) | GET |  |
| [List Message Feedback](actions/list-message-feedback.md) | GET |  |
| [Retrieve Feedback](actions/retrieve-feedback.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST |  |
| [List Messages](actions/list-messages.md) | GET |  |
| [Retrieve Message](actions/retrieve-message.md) | GET |  |
| [Update Message](actions/update-message.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [List Users](actions/list-users.md) | GET |  |
| [Retrieve User](actions/retrieve-user.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

