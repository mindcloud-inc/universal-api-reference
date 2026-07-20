# <img src="https://images.mindcloud.co/apps/icons/peekshot-icon_1776976781927.png" alt="PeekShot logo" width="28" height="28"> PeekShot: Universal API

Capture webpage and HTML screenshots, then retrieve screenshot jobs, lists, and projects from PeekShot.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peekShot/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://peekshot.com
- **Vendor API docs:** https://docs.peekshot.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from PeekShot with optional filtering. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Screenshot from HTML](actions/create-screenshot-from-html.md) | POST | Creates a screenshot from HTML in PeekShot. |
| [Create Screenshot from URL](actions/create-screenshot-from-url.md) | POST | Creates a screenshot from a URL in PeekShot. |
| [Get Screenshot](actions/get-screenshot.md) | GET | Retrieves a screenshot by request ID from PeekShot. |
| [List Screenshots](actions/list-screenshots.md) | GET | Retrieves screenshots from PeekShot with optional filtering. |

