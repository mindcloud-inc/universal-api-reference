# <img src="https://images.mindcloud.co/apps/icons/icon_1775158275437.png" alt="Cloudsmith logo" width="28" height="28"> Cloudsmith: Universal API

Manage repositories, packages, entitlements, users, and software supply chain settings in Cloudsmith.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudsmith/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudsmith.com/
- **Vendor API docs:** https://help.cloudsmith.io/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Distribution

| Action | Method | Description |
| --- | --- | --- |
| [Get Distro](actions/get-distro.md) | GET |  |
| [List Distros](actions/list-distros.md) | GET |  |

### Format

| Action | Method | Description |
| --- | --- | --- |
| [Get Format](actions/get-format.md) | GET |  |
| [List Formats](actions/list-formats.md) | GET |  |

### Namespace

| Action | Method | Description |
| --- | --- | --- |
| [Get Namespace](actions/get-namespace.md) | GET |  |
| [List Namespaces](actions/list-namespaces.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Organization Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Team](actions/create-organization-team.md) | POST |  |
| [Delete Organization Team](actions/delete-organization-team.md) | DELETE |  |
| [Get Organization Team](actions/get-organization-team.md) | GET |  |
| [Update Organization Team](actions/update-organization-team.md) | PUT |  |

### Rate Limits

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Rate Limits](actions/get-current-rate-limits.md) | GET |  |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [Create Repository](actions/create-repository.md) | POST |  |
| [Delete Repository](actions/delete-repository.md) | DELETE |  |
| [Get Repository](actions/get-repository.md) | GET |  |
| [List Repositories for Current User](actions/list-repositories-for-current-user.md) | GET |  |
| [Update Repository](actions/update-repository.md) | PUT |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Basic API Connectivity](actions/check-basic-api-connectivity.md) | GET |  |

