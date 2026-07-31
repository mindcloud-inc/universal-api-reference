# <img src="https://images.mindcloud.co/apps/icons/randomdog_1785420642511.png" alt="random.dog logo" width="28" height="28"> random.dog: Universal API

Retrieve a random dog media URL, optionally including or excluding file extensions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/randomdog/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://random.dog/
- **Vendor API docs:** https://github.com/AdenFlorian/random.dog

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Dog Media](actions/get-random-dog-media.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomdog/latest/actions/get-random-dog-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Dog Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Dog Media](actions/get-random-dog-media.md) | GET |  |

