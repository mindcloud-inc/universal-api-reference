# <img src="https://images.mindcloud.co/apps/icons/netlify_1772806449297.png" alt="Netlify logo" width="28" height="28"> Netlify: Universal API

Build websites, deploy apps, preview changes, and manage serverless functions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/netlify/latest
- **Category:** IT Operations / DevOps
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.netlify.com/
- **Vendor API docs:** https://open-api.netlify.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Build

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Build](actions/get-site-build.md) | GET |  |
| [List Site Builds](actions/list-site-builds.md) | GET |  |

### Build Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Site Build Hook](actions/create-site-build-hook.md) | POST |  |
| [Delete Site Build Hook](actions/delete-site-build-hook.md) | DELETE |  |
| [List Site Build Hooks](actions/list-site-build-hooks.md) | GET |  |
| [Update Site Build Hook](actions/update-site-build-hook.md) | PUT |  |

### Deploy

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Site Deploy](actions/cancel-site-deploy.md) | PUT |  |
| [Create Site Deploy](actions/create-site-deploy.md) | POST |  |
| [Get Site Deploy](actions/get-site-deploy.md) | GET |  |
| [List Site Deploys](actions/list-site-deploys.md) | GET |  |
| [Restore Site Deploy](actions/restore-site-deploy.md) | PUT |  |
| [Rollback Site Deploy](actions/rollback-site-deploy.md) | PUT |  |

### Dns Zone

| Action | Method | Description |
| --- | --- | --- |
| [Configure DNS for Site](actions/configure-dns-for-site.md) | PUT |  |
| [Get DNS for Site](actions/get-dns-for-site.md) | GET |  |

### Environment Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment Variables](actions/create-environment-variables.md) | POST |  |
| [Delete Environment Variable](actions/delete-environment-variable.md) | DELETE |  |
| [Get Environment Variable](actions/get-environment-variable.md) | GET |  |
| [List Environment Variables](actions/list-environment-variables.md) | GET |  |
| [Update Environment Variable](actions/update-environment-variable.md) | PUT |  |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Site Forms](actions/list-site-forms.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST |  |
| [Delete Site](actions/delete-site.md) | DELETE |  |
| [Disable Site](actions/disable-site.md) | PUT |  |
| [Enable Site](actions/enable-site.md) | PUT |  |
| [Get Site](actions/get-site.md) | GET |  |
| [List Sites](actions/list-sites.md) | GET |  |
| [Update Site](actions/update-site.md) | PUT |  |

### Site Function

| Action | Method | Description |
| --- | --- | --- |
| [Search Site Functions](actions/search-site-functions.md) | GET |  |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Form Submissions](actions/list-form-submissions.md) | GET |  |
| [List Site Submissions](actions/list-site-submissions.md) | GET |  |

