# <img src="https://images.mindcloud.co/apps/icons/product-plan_1774908415844.png" alt="ProductPlan logo" width="28" height="28"> ProductPlan: Universal API

ProductPlan is product management and roadmap software for managing roadmaps, discovery, objectives, launches, and product work alignment.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/productPlan/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.productplan.com
- **Vendor API docs:** https://productplan.readme.io/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Status](actions/get-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Backlog Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Bar](actions/get-bar.md) | GET | Retrieves a bar from ProductPlan. |
| [List Child Bars](actions/list-child-bars.md) | GET | Lists child bars for a bar in ProductPlan. |
| [List Roadmap Bars](actions/list-roadmap-bars.md) | GET | Lists bars for a roadmap in ProductPlan. |
| [List Roadmap Lanes](actions/list-roadmap-lanes.md) | GET | Lists lanes for a roadmap in ProductPlan. |

### Checklists

| Action | Method | Description |
| --- | --- | --- |
| [Get Checklist Section](actions/get-checklist-section.md) | GET | Retrieves a checklist section from ProductPlan. |
| [List Checklist Sections](actions/list-checklist-sections.md) | GET | Lists checklist sections for a launch in ProductPlan. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [List Bar Comments](actions/list-bar-comments.md) | GET | Lists comments for a bar in ProductPlan. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [List Bar Connections](actions/list-bar-connections.md) | GET | Lists connections for a bar in ProductPlan. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Lists customers associated with ProductPlan discovery ideas. |

### Feature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Idea](actions/get-idea.md) | GET | Retrieves an idea from ProductPlan. |
| [List Ideas](actions/list-ideas.md) | GET | Lists all ideas accessible in ProductPlan. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Idea Form](actions/get-idea-form.md) | GET | Retrieves an idea form from ProductPlan. |
| [List Idea Forms](actions/list-idea-forms.md) | GET | Lists idea forms in ProductPlan. |

### Key Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Key Result](actions/get-key-result.md) | GET | Retrieves a key result from ProductPlan. |
| [List Key Results](actions/list-key-results.md) | GET | Lists key results for an objective in ProductPlan. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Lists tags associated with ProductPlan discovery ideas. |

### Milestones

| Action | Method | Description |
| --- | --- | --- |
| [List Roadmap Milestones](actions/list-roadmap-milestones.md) | GET | Lists milestones for a roadmap in ProductPlan. |

### Objectives

| Action | Method | Description |
| --- | --- | --- |
| [Get Objective](actions/get-objective.md) | GET | Retrieves an objective from ProductPlan. |
| [List Objectives](actions/list-objectives.md) | GET | Lists all objectives accessible in ProductPlan. |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity](actions/get-opportunity.md) | GET | Retrieves an opportunity from ProductPlan. |
| [List Opportunities](actions/list-opportunities.md) | GET | Lists all opportunities accessible in ProductPlan. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Roadmap](actions/get-roadmap.md) | GET | Retrieves a roadmap from ProductPlan. |
| [List Roadmaps](actions/list-roadmaps.md) | GET | Lists all roadmaps accessible in ProductPlan. |

### Releases

| Action | Method | Description |
| --- | --- | --- |
| [Get Launch](actions/get-launch.md) | GET | Retrieves a launch from ProductPlan. |
| [List Launches](actions/list-launches.md) | GET | Lists all launches in ProductPlan. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Status](actions/get-status.md) | GET | Retrieves application status details from ProductPlan. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from ProductPlan. |
| [List Tasks](actions/list-tasks.md) | GET | Lists tasks for a launch in ProductPlan. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Lists all teams in ProductPlan. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Lists all users in ProductPlan. |

