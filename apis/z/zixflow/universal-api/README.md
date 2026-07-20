# <img src="https://images.mindcloud.co/apps/icons/zixflow_1774230953317.png" alt="Zixflow logo" width="28" height="28"> Zixflow: Universal API

Zixflow is an AI-powered customer engagement platform that combines CRM, lists, activities, and omnichannel outreach across WhatsApp, RCS, SMS, and email.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zixflow/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zixflow.com/
- **Vendor API docs:** https://docs.zixflow.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get List of Workspace Members](actions/get-list-of-workspace-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-workspace-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in Zixflow. |
| [Get Activity By ID](actions/get-activity-by-id.md) | GET | Retrieves an activity from Zixflow. |
| [Get List of Activities](actions/get-list-of-activities.md) | GET | Retrieves activities from Zixflow. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in Zixflow. |

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Attribute](actions/create-custom-attribute.md) | POST | Creates a new custom attribute in Zixflow. |
| [Get Attribute By ID](actions/get-attribute-by-id.md) | GET | Retrieves an attribute from Zixflow. |
| [Get List of Attributes](actions/get-list-of-attributes.md) | GET | Retrieves attributes from Zixflow. |
| [Update Custom Attribute](actions/update-custom-attribute.md) | PUT | Updates an existing custom attribute in Zixflow. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection By ID](actions/get-collection-by-id.md) | GET | Retrieves a collection from Zixflow. |
| [Get List of Collections](actions/get-list-of-collections.md) | GET | Retrieves collections from Zixflow. |

### Collection Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection Record](actions/create-collection-record.md) | POST | Creates a new collection record in Zixflow. |
| [Delete Collection Record By ID](actions/delete-collection-record-by-id.md) | DELETE | Deletes an existing collection record from Zixflow. |
| [Get Collection Record By ID](actions/get-collection-record-by-id.md) | GET | Retrieves a collection record from Zixflow. |
| [Get List of Collection Records](actions/get-list-of-collection-records.md) | GET | Retrieves collection records from Zixflow. |
| [Update Collection Record](actions/update-collection-record.md) | PUT | Updates an existing collection record in Zixflow. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Get List By ID](actions/get-list-by-id.md) | GET | Retrieves a list from Zixflow. |
| [Get List of Lists](actions/get-list-of-lists.md) | GET | Retrieves lists from Zixflow. |

### List Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create List Entry](actions/create-list-entry.md) | POST | Creates a new list entry in Zixflow. |
| [Delete List Entry By ID](actions/delete-list-entry-by-id.md) | DELETE | Deletes an existing list entry from Zixflow. |
| [Get List Entry By ID](actions/get-list-entry-by-id.md) | GET | Retrieves a list entry from Zixflow. |
| [Get List of List Entries](actions/get-list-of-list-entries.md) | GET | Retrieves list entries from Zixflow. |
| [Update List Entry](actions/update-list-entry.md) | PUT | Updates an existing list entry in Zixflow. |

### Template Variable

| Action | Method | Description |
| --- | --- | --- |
| [Get WhatsApp Template Variables](actions/get-whatsapp-template-variables.md) | GET | Retrieves WhatsApp template variables from Zixflow. |

### Workspace Member

| Action | Method | Description |
| --- | --- | --- |
| [Get List of Workspace Members](actions/get-list-of-workspace-members.md) | GET | Retrieves workspace members from Zixflow. |
| [Get Workspace Member By ID](actions/get-workspace-member-by-id.md) | GET | Retrieves a workspace member from Zixflow. |

