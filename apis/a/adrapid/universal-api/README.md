# <img src="https://images.mindcloud.co/apps/icons/images-4_1775151086188.jpeg" alt="Adrapid logo" width="28" height="28"> Adrapid: Universal API

Create, export, and manage marketing banners, templates, and assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/adrapid/latest
- **Category:** Marketing / Advertising
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://adrapid.com
- **Vendor API docs:** https://docs.adrapid.com/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Whitelabel](actions/get-whitelabel.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/get-whitelabel?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Banner

| Action | Method | Description |
| --- | --- | --- |
| [Create User Banner](actions/create-user-banner.md) | POST | Creates a new banner for a user in Adrapid. |
| [Delete User Banner](actions/delete-user-banner.md) | DELETE | Deletes banners for a user in Adrapid. |
| [Get User Banner](actions/get-user-banner.md) | GET | Retrieves a user banner from Adrapid. |
| [Get User Banner Zip](actions/get-user-banner-zip.md) | GET | Retrieves a ZIP download URL for a user banner in Adrapid. |
| [Get User Banners Quota](actions/get-user-banners-quota.md) | GET | Retrieves banner quota for a user in Adrapid. |
| [List User Banners](actions/list-user-banners.md) | GET | Retrieves a user's banners from Adrapid. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Adrapid. |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from Adrapid. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Image](actions/delete-user-image.md) | DELETE | Deletes an existing user image from Adrapid. |
| [Get User Image](actions/get-user-image.md) | GET | Retrieves a user image from Adrapid. |
| [Get User Images Quota](actions/get-user-images-quota.md) | GET | Retrieves image quota for a user in Adrapid. |
| [List User Images](actions/list-user-images.md) | GET | Retrieves a user's images from Adrapid. |
| [Upload User Image](actions/upload-user-image.md) | POST | Uploads a new image for a user in Adrapid. |

### System

| Action | Method | Description |
| --- | --- | --- |
| [Get API Info](actions/get-api-info.md) | GET | Retrieves API service information from Adrapid. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create User Template](actions/create-user-template.md) | POST | Creates a new template for a user in Adrapid. |
| [Delete User Template](actions/delete-user-template.md) | DELETE | Deletes an existing user template from Adrapid. |
| [Get User Template](actions/get-user-template.md) | GET | Retrieves a user template from Adrapid. |
| [Import User Template](actions/import-user-template.md) | POST | Imports a template for a user in Adrapid. |
| [List User Templates](actions/list-user-templates.md) | GET | Retrieves a user's templates from Adrapid. |
| [Update User Template](actions/update-user-template.md) | PUT | Updates an existing user template in Adrapid. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Adrapid. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Adrapid. |
| [Generate User SSO Token](actions/generate-user-sso-token.md) | GET | Generates an SSO login token for a user in Adrapid. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Adrapid by ID. |
| [Get User Access Token](actions/get-user-access-token.md) | GET | Retrieves a user access token from Adrapid. |
| [Get User Access URL](actions/get-user-access-url.md) | GET | Retrieves editor access URLs for a user in Adrapid. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Adrapid. |
| [Refresh User Access Token](actions/refresh-user-access-token.md) | PUT | Refreshes a user's access token in Adrapid. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Adrapid. |

### Whitelabel

| Action | Method | Description |
| --- | --- | --- |
| [Get Whitelabel](actions/get-whitelabel.md) | GET | Retrieves current whitelabel settings from Adrapid. |
| [Update Whitelabel](actions/update-whitelabel.md) | PUT | Updates existing whitelabel settings in Adrapid. |

