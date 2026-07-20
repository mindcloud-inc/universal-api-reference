# <img src="https://images.mindcloud.co/apps/icons/seal-of-the-u_1777930131103.png" alt="Veterans Affairs Forms logo" width="28" height="28"> Veterans Affairs Forms: Universal API

Look up VA forms, search form metadata, retrieve PDF links, and check revision history from the Department of Veterans Affairs VA Forms API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/veteransAffairsForms/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.va.gov/explore/api/va-forms
- **Vendor API docs:** https://developer.va.gov/explore/api/va-forms/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List VA Forms](actions/list-va-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsForms/latest/actions/list-va-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Va Form

| Action | Method | Description |
| --- | --- | --- |
| [Get VA Form](actions/get-va-form.md) | GET | Retrieves a VA form by form name. |
| [List VA Forms](actions/list-va-forms.md) | GET | Finds VA forms by number, keyword, or title. |

