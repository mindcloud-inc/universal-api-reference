# <img src="https://images.mindcloud.co/apps/icons/is-it-christmas_1776437832412.png" alt="Is It Christmas? logo" width="28" height="28"> Is It Christmas?: Universal API

Check whether it is Christmas and browse Christmas history

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/isItChristmas/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://isitchristmas.com
- **Vendor API docs:** https://github.com/isitchristmas/web

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Christmases](actions/list-christmases.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/isItChristmas/latest/actions/list-christmases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Christmas

| Action | Method | Description |
| --- | --- | --- |
| [List Christmases](actions/list-christmases.md) | GET |  |

