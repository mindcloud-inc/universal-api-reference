# <img src="https://images.mindcloud.co/apps/icons/favicon-www-rijksoverheid-nl-48x48_1777488509522.png" alt="Rijksoverheid logo" width="28" height="28"> Rijksoverheid: Universal API

Official public open data from Rijksoverheid.nl, the central Dutch government information site. Current supported API actions expose Dutch school holiday data from the public REST open-data endpoint.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rijksoverheid/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rijksoverheid.nl
- **Vendor API docs:** https://www.rijksoverheid.nl/opendata

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get School Holidays By School Year](actions/get-school-holidays-by-school-year.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksoverheid/latest/actions/get-school-holidays-by-school-year?connectionId=$CONNECTION_ID&schoolYear=2029-2030" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### School Holiday

| Action | Method | Description |
| --- | --- | --- |
| [Get School Holidays By School Year](actions/get-school-holidays-by-school-year.md) | GET | Retrieves school holidays for a school year from Rijksoverheid. |
| [List School Holidays](actions/list-school-holidays.md) | GET | Lists all school holidays from Rijksoverheid. |

