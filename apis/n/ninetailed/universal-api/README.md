# <img src="https://images.mindcloud.co/apps/icons/ninetailed_1777044564151.png" alt="Ninetailed logo" width="28" height="28"> Ninetailed: Universal API

Manage audiences, experiments, and personalized experiences in Contentful

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ninetailed/latest
- **Category:** Marketing
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.contentful.com/products/personalization/
- **Vendor API docs:** https://www.contentful.com/developers/docs/personalization/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organization Spaces](actions/list-organization-spaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-organization-spaces?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Archive Asset](actions/archive-asset.md) | PUT |  |
| [Create Asset](actions/create-asset.md) | POST |  |
| [Create Or Update Asset By ID](actions/create-or-update-asset-by-id.md) | POST |  |
| [Get Asset](actions/get-asset.md) | GET |  |
| [List Assets](actions/list-assets.md) | GET |  |
| [Process Asset](actions/process-asset.md) | PUT |  |
| [Publish Asset](actions/publish-asset.md) | PUT |  |
| [Unpublish Asset](actions/unpublish-asset.md) | PUT |  |

### Content Type

| Action | Method | Description |
| --- | --- | --- |
| [Activate Content Type](actions/activate-content-type.md) | PUT |  |
| [Create Or Update Content Type](actions/create-or-update-content-type.md) | PUT |  |
| [Get Content Type](actions/get-content-type.md) | GET |  |
| [List Content Types](actions/list-content-types.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Archive Entry](actions/archive-entry.md) | PUT |  |
| [Delete Entry](actions/delete-entry.md) | DELETE |  |
| [Patch Entry](actions/patch-entry.md) | PUT |  |
| [Publish Entry](actions/publish-entry.md) | PUT |  |
| [Unarchive Entry](actions/unarchive-entry.md) | PUT |  |
| [Unpublish Entry](actions/unpublish-entry.md) | PUT |  |

### Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | POST |  |
| [Create Or Update Entry By ID](actions/create-or-update-entry-by-id.md) | PUT |  |
| [Get Entry](actions/get-entry.md) | GET |  |
| [List Entries](actions/list-entries.md) | GET |  |
| [List Published Entries](actions/list-published-entries.md) | GET |  |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | POST |  |
| [Delete Environment](actions/delete-environment.md) | DELETE |  |
| [Get Environment](actions/get-environment.md) | GET |  |
| [List Environments](actions/list-environments.md) | GET |  |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Evaluate Profile](actions/evaluate-profile.md) | GET |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET |  |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Spaces](actions/list-organization-spaces.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Tag](actions/create-or-update-tag.md) | POST |  |
| [List Tags](actions/list-tags.md) | GET |  |

### Timezone Settings

| Action | Method | Description |
| --- | --- | --- |
| [Create Locale](actions/create-locale.md) | POST |  |
| [List Locales](actions/list-locales.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Content Type](actions/delete-content-type.md) | DELETE |  |
| [Update Locale](actions/update-locale.md) | PUT |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Webhook](actions/create-or-update-webhook.md) | POST |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Space](actions/get-space.md) | GET |  |

