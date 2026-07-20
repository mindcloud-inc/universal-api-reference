# FBI Most Wanted: Universal API

Access public wanted-person and case records from the FBI Wanted program through the official FBI Wanted API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fBIMostWanted/latest
- **Category:** IT Operations / Database
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fbi.gov/wanted
- **Vendor API docs:** https://www.fbi.gov/wanted/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Wanted Records](actions/list-wanted-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fBIMostWanted/latest/actions/list-wanted-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Wanted Record

| Action | Method | Description |
| --- | --- | --- |
| [List Wanted Records](actions/list-wanted-records.md) | GET | Retrieves wanted records from FBI Most Wanted. |

