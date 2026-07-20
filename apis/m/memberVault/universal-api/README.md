# <img src="https://images.mindcloud.co/apps/icons/member-vault_1773500275513.png" alt="MemberVault logo" width="28" height="28"> MemberVault: Universal API

MemberVault integration for courses and enrollments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/memberVault/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://membervault.co/
- **Vendor API docs:** https://intercom.help/membervault/en/articles/6869595-api-endpoints-advanced

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Course

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from your MemberVault account. |

### Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Product](actions/add-user-to-product.md) | POST | Adds a user to a MemberVault product, creating them if needed. |
| [Remove User from Product](actions/remove-user-from-product.md) | DELETE | Removes a user's access to a product in MemberVault. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user and their data from MemberVault. |

