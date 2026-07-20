# <img src="https://images.mindcloud.co/apps/icons/images-33_1774903116660.png" alt="vPlan logo" width="28" height="28"> vPlan: Universal API

Plan work, manage boards, collections, cards, resources, orders, projects, and webhooks in vPlan.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vPlan/latest
- **Actions:** 56
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vplan.com
- **Vendor API docs:** https://docs.api.vplan.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Authentication Details](actions/retrieve-authentication-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/retrieve-authentication-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (56)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST |  |
| [Get Activity](actions/get-activity.md) | GET |  |
| [List Activities](actions/list-activities.md) | GET |  |
| [Update Activity](actions/update-activity.md) | PUT |  |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Create Attachment Link](actions/create-attachment-link.md) | POST |  |
| [Get Attachment](actions/get-attachment.md) | GET |  |
| [List Attachments](actions/list-attachments.md) | GET |  |

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | POST |  |
| [Get Board](actions/get-board.md) | GET |  |
| [List Boards](actions/list-boards.md) | GET |  |
| [Update Board](actions/update-board.md) | PUT |  |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST |  |
| [Get Collection](actions/get-collection.md) | GET |  |
| [List Collections](actions/list-collections.md) | GET |  |
| [Update Collection](actions/update-collection.md) | PUT |  |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [Get Comment](actions/get-comment.md) | GET |  |
| [List Comments](actions/list-comments.md) | GET |  |
| [Update Comment](actions/update-comment.md) | PUT |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [Create Stage](actions/create-stage.md) | POST |  |
| [Get Stage](actions/get-stage.md) | GET |  |
| [List Stages](actions/list-stages.md) | GET |  |
| [Update Stage](actions/update-stage.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST |  |
| [Create Item](actions/create-item.md) | POST |  |
| [Create Order](actions/create-order.md) | POST |  |
| [Create Relation](actions/create-relation.md) | POST |  |
| [Create Time Tracking Entry](actions/create-time-tracking-entry.md) | POST |  |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Get Card](actions/get-card.md) | GET |  |
| [Get Group](actions/get-group.md) | GET |  |
| [Get Item](actions/get-item.md) | GET |  |
| [Get Order](actions/get-order.md) | GET |  |
| [Get Relation](actions/get-relation.md) | GET |  |
| [Get Resource](actions/get-resource.md) | GET |  |
| [Get Time Tracking Entry](actions/get-time-tracking-entry.md) | GET |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Cards](actions/list-cards.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [List Items](actions/list-items.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [List Relations](actions/list-relations.md) | GET |  |
| [List Resources](actions/list-resources.md) | GET |  |
| [List Time Tracking Entries](actions/list-time-tracking-entries.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Card](actions/update-card.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Retrieve Authentication Details](actions/retrieve-authentication-details.md) | GET |  |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [Create Warehouse](actions/create-warehouse.md) | POST |  |
| [Get Warehouse](actions/get-warehouse.md) | GET |  |
| [List Warehouses](actions/list-warehouses.md) | GET |  |

