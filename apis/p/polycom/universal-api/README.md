# <img src="https://images.mindcloud.co/apps/icons/polycom_1775661417160.png" alt="Polycom logo" width="28" height="28"> Polycom: Universal API

Poly Lens gives you access to Poly tenant, device, room, software, and operational management data through the Poly Lens GraphQL API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/polycom/latest
- **Category:** Communication / Video Communications
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lens.poly.com
- **Vendor API docs:** https://api.lens.poly.com/docs/graphql/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tenants](actions/list-tenants.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Search Devices](actions/search-devices.md) | GET | Searches Poly Lens devices and returns inventory details for each result. |
| [Search Studio X Teams and Zoom Devices](actions/search-studio-x-teams-and-zoom-devices.md) | GET | Searches Studio X devices in Poly Lens running Teams or Zoom. |
| [Search Teams and Zoom Devices](actions/search-teams-and-zoom-devices.md) | GET | Searches Poly Lens devices whose active application is Microsoft or Zoom. |
| [Search Zoom Devices](actions/search-zoom-devices.md) | GET | Searches Poly Lens devices whose active application is Zoom. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Tenants](actions/list-tenants.md) | GET | Lists Poly Lens tenants with member, device, and room totals. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Count Tenant Admins](actions/count-tenant-admins.md) | GET | Counts admin users in a selected Poly Lens tenant. |
| [List Tenant Admins](actions/list-tenant-admins.md) | GET | Lists admin users for a selected Poly Lens tenant. |
| [List Tenant Members By Role](actions/list-tenant-members-by-role.md) | GET | Lists tenant members in Poly Lens for a selected role. |

