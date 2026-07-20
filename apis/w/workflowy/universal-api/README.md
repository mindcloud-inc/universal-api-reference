# <img src="https://images.mindcloud.co/apps/icons/workflowy_1773340317066.png" alt="Workflowy logo" width="28" height="28"> Workflowy: Universal API

Manage Workflowy nodes, search lists, and organize content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/workflowy/latest
- **Category:** Content & Files / Storage
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://workflowy.com
- **Vendor API docs:** https://beta.workflowy.com/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Targets](actions/list-targets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/list-targets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Node

| Action | Method | Description |
| --- | --- | --- |
| [Complete Node](actions/complete-node.md) | PUT | Marks a Workflowy node as completed. |
| [Create Node](actions/create-node.md) | POST | Creates a new node in Workflowy. |
| [Delete Node](actions/delete-node.md) | DELETE | Deletes an existing node from Workflowy. |
| [Export All Nodes](actions/export-all-nodes.md) | GET | Retrieves all Workflowy nodes as a flat list. |
| [List Nodes](actions/list-nodes.md) | GET | Retrieves child nodes from Workflowy for a parent. |
| [Move Node](actions/move-node.md) | PUT | Moves a node to a new parent in Workflowy. |
| [Retrieve Node](actions/retrieve-node.md) | GET | Retrieves a Workflowy node by target or ID. |
| [Uncomplete Node](actions/uncomplete-node.md) | PUT | Marks a Workflowy node as not completed. |
| [Update Node](actions/update-node.md) | PUT | Updates an existing node in Workflowy. |

### Target

| Action | Method | Description |
| --- | --- | --- |
| [List Targets](actions/list-targets.md) | GET | Retrieves available targets from the Workflowy account. |

