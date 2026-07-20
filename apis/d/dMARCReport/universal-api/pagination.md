# DMARC Report Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DMARC Report expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/get-aggregate-report-records?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DMARC Report actions that support pagination

- [Get Aggregate Report Records](actions/get-aggregate-report-records.md)
- [List Account Domains](actions/list-account-domains.md)
- [List Accounts](actions/list-accounts.md)
- [List Aggregate Reports](actions/list-aggregate-reports.md)
- [List Domains](actions/list-domains.md)
- [List Forensic Reports](actions/list-forensic-reports.md)
- [List MTA-STS Failure Details](actions/list-mta-sts-failure-details.md)
- [List MTA-STS Reports](actions/list-mta-sts-reports.md)
