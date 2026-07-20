# ProductPlan: Native API Reference

A consolidated summary of ProductPlan's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://productplan.readme.io/reference/overview
- **API base URL:** `https://app.productplan.com/api/v2`

## Authentication

### API Token

Use a ProductPlan personal API token generated from Integrations -> Custom.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://productplan.readme.io/reference/authentication)

## API conventions

The total page count is read from `paging.page_count`. The current page number is read from `paging.current_page`.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Bar](actions/get-bar.md) | `GET /bars/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-bars-id) |
| [Get Checklist Section](actions/get-checklist-section.md) | `GET /launches/:launch_id/checklist_sections/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-launches-launch-id-checklist-sections-id) |
| [Get Idea](actions/get-idea.md) | `GET /discovery/ideas/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-discovery-ideas-id) |
| [Get Idea Form](actions/get-idea-form.md) | `GET /discovery/idea_forms/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-discovery-idea-forms-id) |
| [Get Key Result](actions/get-key-result.md) | `GET /strategy/objectives/:objective_id/key_results/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-strategy-objectives-objective-id-key-results-id) |
| [Get Launch](actions/get-launch.md) | `GET /launches/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-launches-id) |
| [Get Objective](actions/get-objective.md) | `GET /strategy/objectives/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-strategy-objectives-id) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /discovery/opportunities/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-discovery-opportunities-id) |
| [Get Roadmap](actions/get-roadmap.md) | `GET /roadmaps/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-roadmaps-id) |
| [Get Status](actions/get-status.md) | `GET /status` | [docs](https://productplan.readme.io/reference/get_api-v2-status) |
| [Get Task](actions/get-task.md) | `GET /launches/:launch_id/tasks/:id` | [docs](https://productplan.readme.io/reference/get_api-v2-launches-launch-id-tasks-id) |
| [List Bar Comments](actions/list-bar-comments.md) | `GET /bars/:id/comments` | [docs](https://productplan.readme.io/reference/get_api-v2-bars-id-comments) |
| [List Bar Connections](actions/list-bar-connections.md) | `GET /bars/:bar_id/connections` | [docs](https://productplan.readme.io/reference/get_api-v2-bars-bar-id-connections) |
| [List Checklist Sections](actions/list-checklist-sections.md) | `GET /launches/:launch_id/checklist_sections` | [docs](https://productplan.readme.io/reference/get_api-v2-launches-launch-id-checklist-sections) |
| [List Child Bars](actions/list-child-bars.md) | `GET /bars/:id/child_bars` | [docs](https://productplan.readme.io/reference/get_api-v2-bars-id-child-bars) |
| [List Customers](actions/list-customers.md) | `GET /discovery/ideas/customers` | [docs](https://productplan.readme.io/reference/get_api-v2-discovery-ideas-customers) |
| [List Idea Forms](actions/list-idea-forms.md) | `GET /discovery/idea_forms` | [docs](https://productplan.readme.io/reference/get_api-v2-discovery-idea-forms) |
| [List Ideas](actions/list-ideas.md) | `GET /discovery/ideas` | [docs](https://productplan.readme.io/reference/get_api-v2-discovery-ideas) |
| [List Key Results](actions/list-key-results.md) | `GET /strategy/objectives/:objective_id/key_results` | [docs](https://productplan.readme.io/reference/get_api-v2-strategy-objectives-objective-id-key-results) |
| [List Launches](actions/list-launches.md) | `GET /launches` | [docs](https://productplan.readme.io/reference/get_api-v2-launches) |
| [List Objectives](actions/list-objectives.md) | `GET /strategy/objectives` | [docs](https://productplan.readme.io/reference/get_api-v2-strategy-objectives) |
| [List Opportunities](actions/list-opportunities.md) | `GET /discovery/opportunities` | [docs](https://productplan.readme.io/reference/get_api-v2-discovery-opportunities) |
| [List Roadmap Bars](actions/list-roadmap-bars.md) | `GET /roadmaps/:id/bars` | [docs](https://productplan.readme.io/reference/get_api-v2-roadmaps-id-bars) |
| [List Roadmap Lanes](actions/list-roadmap-lanes.md) | `GET /roadmaps/:roadmap_id/lanes` | [docs](https://productplan.readme.io/reference/get_api-v2-roadmaps-roadmap-id-lanes) |
| [List Roadmap Milestones](actions/list-roadmap-milestones.md) | `GET /roadmaps/:roadmap_id/milestones` | [docs](https://productplan.readme.io/reference/get_api-v2-roadmaps-roadmap-id-milestones) |
| [List Roadmaps](actions/list-roadmaps.md) | `GET /roadmaps` | [docs](https://productplan.readme.io/reference/get_api-v2-roadmaps) |
| [List Tags](actions/list-tags.md) | `GET /discovery/ideas/tags` | [docs](https://productplan.readme.io/reference/get_api-v2-discovery-ideas-tags) |
| [List Tasks](actions/list-tasks.md) | `GET /launches/:launch_id/tasks` | [docs](https://productplan.readme.io/reference/get_api-v2-launches-launch-id-tasks) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://productplan.readme.io/reference/get_api-v2-teams) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://productplan.readme.io/reference/get_api-v2-users) |
