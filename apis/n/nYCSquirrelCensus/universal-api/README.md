# <img src="https://images.mindcloud.co/apps/icons/n-ycsquirrel-census_1785420737431.png" alt="NYC Squirrel Census logo" width="28" height="28"> NYC Squirrel Census: Universal API

Read historical 2018 Central Park squirrel sightings from the NYC Open Data Socrata dataset.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nYCSquirrelCensus/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://data.cityofnewyork.us/Environment/2018-Central-Park-Squirrel-Census-Squirrel-Data/vfnx-vebw
- **Vendor API docs:** https://dev.socrata.com/foundry/data.cityofnewyork.us/vfnx-vebw

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List squirrel sightings](actions/list-squirrel-sightings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nYCSquirrelCensus/latest/actions/list-squirrel-sightings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Squirrel Sighting

| Action | Method | Description |
| --- | --- | --- |
| [List squirrel sightings](actions/list-squirrel-sightings.md) | GET |  |

