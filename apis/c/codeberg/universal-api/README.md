# <img src="https://images.mindcloud.co/apps/icons/codeberg_1776692449644.png" alt="Codeberg logo" width="28" height="28"> Codeberg: Universal API

Codeberg is a Forgejo-powered source code hosting platform for repositories, issues, pull requests, organizations, releases, notifications, and account resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/codeberg/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://codeberg.org
- **Vendor API docs:** https://forgejo.org/docs/v13.0/user/api-usage/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activitypub

| Action | Method | Description |
| --- | --- | --- |
| [Get ActivityPub Instance Actor](actions/get-activitypub-instance-actor.md) | GET |  |

### Artifact

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Quota Artifacts](actions/list-current-user-quota-artifacts.md) | GET |  |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Quota Attachments](actions/list-current-user-quota-attachments.md) | GET |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [List User Emails](actions/list-user-emails.md) | GET |  |

### Gpg Key

| Action | Method | Description |
| --- | --- | --- |
| [List Current User GPG Keys](actions/list-current-user-gpg-keys.md) | GET |  |

### Instance

| Action | Method | Description |
| --- | --- | --- |
| [Get Node Info](actions/get-node-info.md) | GET |  |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Search Issues](actions/search-issues.md) | GET |  |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Check New Notifications](actions/check-new-notifications.md) | GET |  |
| [List Notifications](actions/list-notifications.md) | GET |  |

### Oauth2 Application

| Action | Method | Description |
| --- | --- | --- |
| [List User OAuth2 Applications](actions/list-user-oauth2-applications.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Organizations](actions/list-current-user-organizations.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Quota Packages](actions/list-current-user-quota-packages.md) | GET |  |

### Public Key

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Public Keys](actions/list-current-user-public-keys.md) | GET |  |

### Quota

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Quota](actions/get-current-user-quota.md) | GET |  |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Repositories](actions/list-current-user-repositories.md) | GET |  |
| [List Starred Repositories](actions/list-starred-repositories.md) | GET |  |
| [List Watched Repositories](actions/list-watched-repositories.md) | GET |  |
| [Search Repositories](actions/search-repositories.md) | GET |  |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get API Settings](actions/get-api-settings.md) | GET |  |
| [Get Attachment Settings](actions/get-attachment-settings.md) | GET |  |
| [Get Repository Settings](actions/get-repository-settings.md) | GET |  |
| [Get UI Settings](actions/get-ui-settings.md) | GET |  |

### Signing Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Default GPG Signing Key](actions/get-default-gpg-signing-key.md) | GET |  |
| [Get Default SSH Signing Key](actions/get-default-ssh-signing-key.md) | GET |  |

### Stopwatch

| Action | Method | Description |
| --- | --- | --- |
| [List Stopwatches](actions/list-stopwatches.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List User Teams](actions/list-user-teams.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Gitignore Templates](actions/list-gitignore-templates.md) | GET |  |
| [List Label Templates](actions/list-label-templates.md) | GET |  |
| [List License Templates](actions/list-license-templates.md) | GET |  |

### Tracked Time

| Action | Method | Description |
| --- | --- | --- |
| [List User Tracked Times](actions/list-user-tracked-times.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [List Blocked Users](actions/list-blocked-users.md) | GET |  |
| [List Current User Followers](actions/list-current-user-followers.md) | GET |  |
| [List Current User Following](actions/list-current-user-following.md) | GET |  |
| [Search Users](actions/search-users.md) | GET |  |

### User Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Settings](actions/get-current-user-settings.md) | GET |  |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [List User Actions Variables](actions/list-user-actions-variables.md) | GET |  |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Forgejo Version](actions/get-forgejo-version.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Webhooks](actions/list-current-user-webhooks.md) | GET |  |

