# <img src="https://images.mindcloud.co/apps/icons/cinode_1774887095489.png" alt="Cinode logo" width="28" height="28"> Cinode: Universal API

Cinode: Manage consulting skills, sales, staffing, and projects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cinode/latest
- **Category:** Productivity / Project Management
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cinode.com
- **Vendor API docs:** https://api.cinode.com/docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Auth

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | GET | Retrieves an access token from Cinode. |

### Customer Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer Tag](actions/add-customer-tag.md) | POST | Adds a tag to a customer in Cinode. |
| [List Customer Tags](actions/list-customer-tags.md) | GET | Retrieves tags for a customer in Cinode. |
| [Remove Customer Tag](actions/remove-customer-tag.md) | DELETE | Removes a tag from a customer in Cinode. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Cinode. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Cinode. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a company customer list from Cinode. |

### Project Assignment Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Assignment Tag](actions/add-project-assignment-tag.md) | POST | Adds a tag to a project assignment in Cinode. |
| [List Project Assignment Tags](actions/list-project-assignment-tags.md) | GET | Retrieves tags for a project assignment in Cinode. |
| [Remove Project Assignment Tag](actions/remove-project-assignment-tag.md) | DELETE | Removes a tag from a project assignment in Cinode. |

### Project Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Tag](actions/add-project-tag.md) | POST | Adds a tag to a project in Cinode. |
| [List Project Tags](actions/list-project-tags.md) | GET | Retrieves tags for a project in Cinode. |
| [Remove Project Tag](actions/remove-project-tag.md) | DELETE | Removes a tag from a project in Cinode. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Cinode. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Cinode. |
| [List Projects](actions/list-projects.md) | GET | Retrieves won projects for a company in Cinode. |

### Tag Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag Type](actions/create-tag-type.md) | POST | Creates a tag type in Cinode. |
| [Delete Tag Type](actions/delete-tag-type.md) | DELETE | Deletes an existing tag type from Cinode. |
| [Get Tag Type](actions/get-tag-type.md) | GET | Retrieves a tag type from Cinode. |
| [List Tag Types](actions/list-tag-types.md) | GET | Retrieves company tag types from Cinode. |
| [Update Tag Type](actions/update-tag-type.md) | PUT | Updates an existing tag type in Cinode. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user identity from Cinode. |

