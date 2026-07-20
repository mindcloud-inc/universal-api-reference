# <img src="https://images.mindcloud.co/apps/icons/favicon-developer-schiphol-nl-48x48_1777546432948.png" alt="SchoolDigger logo" width="28" height="28"> SchoolDigger: Universal API

Access K-12 school and district directory, ranking, demographic, test score, finance, and autocomplete data from SchoolDigger.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/schoolDigger/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.schooldigger.com
- **Vendor API docs:** https://developer.schooldigger.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Autocomplete Districts](actions/autocomplete-districts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/autocomplete-districts?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### District

| Action | Method | Description |
| --- | --- | --- |
| [Get District](actions/get-district.md) | GET | Retrieves a district from SchoolDigger. |
| [Search Districts](actions/search-districts.md) | GET | Finds districts in SchoolDigger by search criteria. |

### District Autocomplete Result

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Districts](actions/autocomplete-districts.md) | GET | Finds district matches in SchoolDigger by partial search text. |

### District Ranking

| Action | Method | Description |
| --- | --- | --- |
| [List District Rankings](actions/list-district-rankings.md) | GET | Retrieves district rankings from SchoolDigger. |

### School

| Action | Method | Description |
| --- | --- | --- |
| [Get School](actions/get-school.md) | GET | Retrieves a school from SchoolDigger. |
| [Search Schools](actions/search-schools.md) | GET | Finds schools in SchoolDigger by search criteria. |

### School Autocomplete Result

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Schools](actions/autocomplete-schools.md) | GET | Finds school matches in SchoolDigger by partial search text. |

### School Ranking

| Action | Method | Description |
| --- | --- | --- |
| [List School Rankings](actions/list-school-rankings.md) | GET | Retrieves school rankings from SchoolDigger. |

