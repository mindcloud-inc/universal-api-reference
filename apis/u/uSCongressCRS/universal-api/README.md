# <img src="https://images.mindcloud.co/apps/icons/favicon-github-com-48x48-1_1778073894202.png" alt="US Congress CRS logo" width="28" height="28"> US Congress CRS: Universal API

Search and retrieve Congressional Research Service report metadata from the official Congress.gov API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uSCongressCRS/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.congress.gov
- **Vendor API docs:** https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CRSReportEndpoint.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List CRS Reports](actions/list-crs-reports.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSCongressCRS/latest/actions/list-crs-reports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Crs Report

| Action | Method | Description |
| --- | --- | --- |
| [Get CRS Report](actions/get-crs-report.md) | GET | Retrieves a CRS report from US Congress CRS. |
| [List CRS Reports](actions/list-crs-reports.md) | GET | Retrieves CRS reports from US Congress CRS. |

