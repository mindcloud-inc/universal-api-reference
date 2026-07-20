# Digital Humani: Universal API

Plant trees, browse projects, and report reforestation activity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/digitalHumani/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.digitalhumani.com/
- **Vendor API docs:** https://docs.digitalhumani.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Authenticated User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from Digital Humani. |

### Enterprise

| Action | Method | Description |
| --- | --- | --- |
| [Get Enterprise](actions/get-enterprise.md) | GET | Retrieves an enterprise from Digital Humani by ID. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a reforestation project from Digital Humani by ID. |
| [List Projects](actions/list-projects.md) | GET | Lists reforestation projects in Digital Humani. |

### Tree Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Enterprise Total Tree Count](actions/get-enterprise-total-tree-count.md) | GET | Retrieves an enterprise's total tree count from Digital Humani. |
| [Get Enterprise Tree Count by Date Range](actions/get-enterprise-tree-count-by-date-range.md) | GET | Retrieves an enterprise tree count from Digital Humani by date range. |
| [Get Enterprise Tree Count by Month](actions/get-enterprise-tree-count-by-month.md) | GET | Retrieves an enterprise's monthly tree count from Digital Humani. |
| [Get User Tree Count](actions/get-user-tree-count.md) | GET | Retrieves a user's tree count from Digital Humani. |

### Tree Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Tree Request](actions/get-tree-request.md) | GET | Retrieves a tree-planting request from Digital Humani by UUID. |
| [Plant Trees](actions/plant-trees.md) | POST | Creates a tree-planting request in Digital Humani. |

