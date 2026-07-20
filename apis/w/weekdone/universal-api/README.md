# <img src="https://images.mindcloud.co/apps/icons/weekdone_1774294537228.png" alt="Weekdone logo" width="28" height="28"> Weekdone: Universal API

Weekdone is an OKR, weekly reporting, and team planning platform. This wrapper lets MindCloud read and manage Weekdone items, reports, tags, objectives, KPIs, teams, users, and company metadata through the official Weekdone API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weekdone/latest
- **Category:** Productivity / Project Management
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://weekdone.com/
- **Vendor API docs:** https://weekdone.com/developer

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Info](actions/get-company-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/get-company-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Types](actions/list-types.md) | GET | Lists item types in Weekdone. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Item Comment](actions/add-item-comment.md) | POST | Creates a comment on an item in Weekdone. |
| [Add Objective Comment](actions/add-objective-comment.md) | POST | Creates a comment on an objective in Weekdone. |
| [Delete Item Comment](actions/delete-item-comment.md) | DELETE | Deletes a comment from an item in Weekdone. |
| [Delete Objective Comment](actions/delete-objective-comment.md) | DELETE | Deletes a comment from an objective in Weekdone. |
| [List Item Comments](actions/list-item-comments.md) | GET | Lists comments for an item in Weekdone. |
| [List Objective Comments](actions/list-objective-comments.md) | GET | Lists comments for an objective in Weekdone. |
| [Update Objective Comment](actions/update-objective-comment.md) | PUT | Updates an objective comment in Weekdone. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Info](actions/get-company-info.md) | GET | Retrieves company details from Weekdone. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Assign Item](actions/assign-item.md) | PUT | Assigns an item to a user in Weekdone. |
| [Create Item](actions/create-item.md) | POST | Creates a new item in Weekdone. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an existing item from Weekdone. |
| [Search Items](actions/search-items.md) | GET | Finds items in Weekdone. |
| [Sort Items](actions/sort-items.md) | PUT | Updates item order for a week in Weekdone. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Weekdone. |

### Key Results

| Action | Method | Description |
| --- | --- | --- |
| [Add Objective Result](actions/add-objective-result.md) | POST | Creates a key result for an objective in Weekdone. |
| [Delete Objective Result](actions/delete-objective-result.md) | DELETE | Deletes a key result from an objective in Weekdone. |
| [Update Objective Result](actions/update-objective-result.md) | PUT | Updates a key result for an objective in Weekdone. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Create KPI](actions/create-kpi.md) | POST | Creates a new KPI in Weekdone. |
| [Delete KPI](actions/delete-kpi.md) | DELETE | Deletes an existing KPI from Weekdone. |
| [List KPIs](actions/list-kpis.md) | GET | Lists KPIs in Weekdone. |
| [Update KPI](actions/update-kpi.md) | PUT | Updates an existing KPI in Weekdone. |
| [Update KPI Value](actions/update-kpi-value.md) | PUT | Updates progress for a KPI in Weekdone. |

### Objectives

| Action | Method | Description |
| --- | --- | --- |
| [Create Objective](actions/create-objective.md) | POST | Creates a new objective in Weekdone. |
| [Delete Objective](actions/delete-objective.md) | DELETE | Deletes an existing objective from Weekdone. |
| [List Objectives](actions/list-objectives.md) | GET | Lists objectives in Weekdone. |
| [Update Objective](actions/update-objective.md) | PUT | Updates an existing objective in Weekdone. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [Add Item Like](actions/add-item-like.md) | POST | Creates a like for an item in Weekdone. |
| [Delete Item Like](actions/delete-item-like.md) | DELETE | Deletes a like from an item in Weekdone. |
| [List Item Likes](actions/list-item-likes.md) | GET | Lists likes for an item in Weekdone. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Report](actions/get-report.md) | GET | Retrieves the current report from Weekdone. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a specific tag from Weekdone. |
| [List Tags](actions/list-tags.md) | GET | Lists tags in Weekdone. |
| [Update Tag Priority](actions/update-tag-priority.md) | PUT | Updates priority status for a tag in Weekdone. |
| [Update Tag Status](actions/update-tag-status.md) | PUT | Updates status text for a tag in Weekdone. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Lists teams in Weekdone. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Lists users in Weekdone. |

