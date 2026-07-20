# <img src="https://images.mindcloud.co/apps/icons/talk-python-to-me_1776450345091.png" alt="Talk Python To Me logo" width="28" height="28"> Talk Python To Me: Universal API

Search Talk Python To Me episodes and transcript content from the public Talk Python search API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/talkPythonToMe/latest
- **Category:** Website & App Building / CMS
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://talkpython.fm
- **Vendor API docs:** https://search.talkpython.fm/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Episodes and Transcripts](actions/search-episodes-and-transcripts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talkPythonToMe/latest/actions/search-episodes-and-transcripts?connectionId=$CONNECTION_ID&query=python-testing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Episodes and Transcripts](actions/search-episodes-and-transcripts.md) | GET | Finds episodes and transcripts in Talk Python To Me. |

