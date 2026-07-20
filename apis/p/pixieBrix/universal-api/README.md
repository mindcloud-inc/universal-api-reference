# <img src="https://images.mindcloud.co/apps/icons/pixiebrix-icon_1777920857881.png" alt="PixieBrix logo" width="28" height="28"> PixieBrix: Universal API

Build and manage PixieBrix teams, packages, deployments, databases, records, and related admin resources through the PixieBrix Developer API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pixieBrix/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pixiebrix.com
- **Vendor API docs:** https://docs.pixiebrix.com/developer-api/making-an-api-request

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Health Check](actions/health-check.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Asset](actions/get-database-asset.md) | GET | Retrieves a database asset from PixieBrix. |
| [List Database Assets](actions/list-database-assets.md) | GET | Retrieves assets from a PixieBrix database. |

### Database Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Database Record](actions/create-database-record.md) | POST | Creates a database record in PixieBrix, merging by key if needed. |
| [Get Database Record](actions/get-database-record.md) | GET | Retrieves a record from a PixieBrix database. |
| [List Database Records](actions/list-database-records.md) | GET | Retrieves records from a PixieBrix database. |
| [Update Database Record](actions/update-database-record.md) | PUT | Updates a database record in PixieBrix, creating it if needed. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Get Database](actions/get-database.md) | GET | Retrieves a database from PixieBrix. |
| [List Databases](actions/list-databases.md) | GET | Retrieves databases from a PixieBrix organization. |

### Deployment Error

| Action | Method | Description |
| --- | --- | --- |
| [List Deployment Errors](actions/list-deployment-errors.md) | GET | Retrieves recent deployment errors from PixieBrix. |

### Deployments

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment](actions/get-deployment.md) | GET | Retrieves a deployment from PixieBrix. |
| [List Deployments](actions/list-deployments.md) | GET | Retrieves deployments from a PixieBrix organization. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from PixieBrix. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups in a PixieBrix organization. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Memberships](actions/list-organization-memberships.md) | GET | Retrieves memberships for an organization in PixieBrix. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from PixieBrix. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves the current user's organizations from PixieBrix. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Get Package](actions/get-package.md) | GET | Retrieves a package from PixieBrix. |
| [List Packages](actions/list-packages.md) | GET | Retrieves packages from a PixieBrix organization. |

### Package Version

| Action | Method | Description |
| --- | --- | --- |
| [List Package Versions](actions/list-package-versions.md) | GET | Retrieves versions for a PixieBrix package. |

### Registry Brick

| Action | Method | Description |
| --- | --- | --- |
| [Get Registry Brick](actions/get-registry-brick.md) | GET | Retrieves a brick package from the PixieBrix registry. |
| [List Registry Bricks](actions/list-registry-bricks.md) | GET | Retrieves brick packages from the PixieBrix registry. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves the PixieBrix API health status. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from PixieBrix. |
| [Get Organization Member](actions/get-organization-member.md) | GET | Retrieves an organization member from PixieBrix. |

