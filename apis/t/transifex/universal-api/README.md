# <img src="https://images.mindcloud.co/apps/icons/images-13_1775842345375.png" alt="Transifex logo" width="28" height="28"> Transifex: Universal API

Access Transifex organizations, projects, resources, source strings, and translations through the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/transifex/latest
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.transifex.com
- **Vendor API docs:** https://developers.transifex.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Language](actions/add-project-language.md) | POST |  |
| [Bulk Update Resource Translations](actions/bulk-update-resource-translations.md) | PUT |  |
| [Create Resource](actions/create-resource.md) | POST |  |
| [Create Resource String](actions/create-resource-string.md) | POST |  |
| [Create Resource String Comment](actions/create-resource-string-comment.md) | POST |  |
| [Delete Project Language Relationship](actions/delete-project-language-relationship.md) | DELETE |  |
| [Delete Resource](actions/delete-resource.md) | DELETE |  |
| [Delete Resource String Comment](actions/delete-resource-string-comment.md) | DELETE |  |
| [Get Language](actions/get-language.md) | GET |  |
| [Get Resource](actions/get-resource.md) | GET |  |
| [Get Resource String](actions/get-resource-string.md) | GET |  |
| [Get Resource String Comment](actions/get-resource-string-comment.md) | GET |  |
| [Get Resource Translation](actions/get-resource-translation.md) | GET |  |
| [Get Translation Download](actions/get-translation-download.md) | GET |  |
| [List Languages](actions/list-languages.md) | GET |  |
| [List Project Languages](actions/list-project-languages.md) | GET |  |
| [List Resource String Comments](actions/list-resource-string-comments.md) | GET |  |
| [List Resource Strings](actions/list-resource-strings.md) | GET |  |
| [List Resource Translations](actions/list-resource-translations.md) | GET |  |
| [List Resources](actions/list-resources.md) | GET |  |
| [Start Translation Download](actions/start-translation-download.md) | POST |  |
| [Update Resource](actions/update-resource.md) | PUT |  |
| [Update Resource String](actions/update-resource-string.md) | PUT |  |
| [Update Resource String Comment](actions/update-resource-string-comment.md) | PUT |  |
| [Update Resource Translation](actions/update-resource-translation.md) | PUT |  |

