# Congress.gov: Native API Reference

A consolidated summary of Congress.gov's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://github.com/LibraryOfCongress/api.congress.gov
- **OpenAPI specification:** https://raw.githubusercontent.com/LibraryOfCongress/api.congress.gov/main/Documentation/swagger.json
- **API base URL:** `https://api.congress.gov/v3`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/LibraryOfCongress/api.congress.gov)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `pagination.next`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–250). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Use `updateDate+asc` for ascending order and `updateDate+desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Amendment](actions/get-amendment.md) | `GET /amendment/:congress/:amendmentType/:amendmentNumber` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/AmendmentEndpoint.md) |
| [Get Bill](actions/get-bill.md) | `GET /bill/:congress/:billType/:billNumber` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [Get Committee](actions/get-committee.md) | `GET /committee/:chamber/:committeeCode` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeEndpoint.md) |
| [Get Committee Print](actions/get-committee-print.md) | `GET /committee-print/:congress/:chamber/:jacketNumber` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteePrintEndpoint.md) |
| [Get Committee Report](actions/get-committee-report.md) | `GET /committee-report/:congress/:reportType/:reportNumber` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeReportEndpoint.md) |
| [Get Congress](actions/get-congress.md) | `GET /congress/:congress` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CongressEndpoint.md) |
| [Get Current Congress](actions/get-current-congress.md) | `GET /congress/current` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CongressEndpoint.md) |
| [Get Law](actions/get-law.md) | `GET /law/:congress/:lawType/:lawNumber` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [Get Member](actions/get-member.md) | `GET /member/:bioguideId` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/MemberEndpoint.md) |
| [List Amendment Actions](actions/list-amendment-actions.md) | `GET /amendment/:congress/:amendmentType/:amendmentNumber/actions` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/AmendmentEndpoint.md) |
| [List Amendment Cosponsors](actions/list-amendment-cosponsors.md) | `GET /amendment/:congress/:amendmentType/:amendmentNumber/cosponsors` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/AmendmentEndpoint.md) |
| [List Amendments](actions/list-amendments.md) | `GET /amendment` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/AmendmentEndpoint.md) |
| [List Bill Actions](actions/list-bill-actions.md) | `GET /bill/:congress/:billType/:billNumber/actions` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bill Amendments](actions/list-bill-amendments.md) | `GET /bill/:congress/:billType/:billNumber/amendments` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bill Committees](actions/list-bill-committees.md) | `GET /bill/:congress/:billType/:billNumber/committees` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bill Cosponsors](actions/list-bill-cosponsors.md) | `GET /bill/:congress/:billType/:billNumber/cosponsors` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bill Subjects](actions/list-bill-subjects.md) | `GET /bill/:congress/:billType/:billNumber/subjects` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bill Summaries](actions/list-bill-summaries.md) | `GET /bill/:congress/:billType/:billNumber/summaries` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bill Text Versions](actions/list-bill-text-versions.md) | `GET /bill/:congress/:billType/:billNumber/text` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bill Titles](actions/list-bill-titles.md) | `GET /bill/:congress/:billType/:billNumber/titles` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bills](actions/list-bills.md) | `GET /bill` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bills By Congress](actions/list-bills-by-congress.md) | `GET /bill/:congress` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Bills By Congress And Type](actions/list-bills-by-congress-and-type.md) | `GET /bill/:congress/:billType` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Committee Bills](actions/list-committee-bills.md) | `GET /committee/:chamber/:committeeCode/bills` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeEndpoint.md) |
| [List Committee Meetings](actions/list-committee-meetings.md) | `GET /committee-meeting` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeMeetingEndpoint.md) |
| [List Committee Prints](actions/list-committee-prints.md) | `GET /committee-print` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteePrintEndpoint.md) |
| [List Committee Reports](actions/list-committee-reports.md) | `GET /committee-report` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeReportEndpoint.md) |
| [List Committees](actions/list-committees.md) | `GET /committee` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeEndpoint.md) |
| [List Congresses](actions/list-congresses.md) | `GET /congress` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CongressEndpoint.md) |
| [List Hearings](actions/list-hearings.md) | `GET /hearing` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/HearingEndpoint.md) |
| [List Laws By Congress](actions/list-laws-by-congress.md) | `GET /law/:congress` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Laws By Congress And Type](actions/list-laws-by-congress-and-type.md) | `GET /law/:congress/:lawType` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Member Cosponsored Legislation](actions/list-member-cosponsored-legislation.md) | `GET /member/:bioguideId/cosponsored-legislation` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/MemberEndpoint.md) |
| [List Member Sponsored Legislation](actions/list-member-sponsored-legislation.md) | `GET /member/:bioguideId/sponsored-legislation` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/MemberEndpoint.md) |
| [List Members](actions/list-members.md) | `GET /member` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/MemberEndpoint.md) |
| [List Members By Congress](actions/list-members-by-congress.md) | `GET /member/congress/:congress` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/MemberEndpoint.md) |
| [List Related Bills](actions/list-related-bills.md) | `GET /bill/:congress/:billType/:billNumber/relatedbills` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md) |
| [List Summaries](actions/list-summaries.md) | `GET /summaries` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/SummariesEndpoint.md) |
| [List Summaries By Congress](actions/list-summaries-by-congress.md) | `GET /summaries/:congress` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/SummariesEndpoint.md) |
| [List Summaries By Congress And Bill Type](actions/list-summaries-by-congress-and-bill-type.md) | `GET /summaries/:congress/:billType` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/SummariesEndpoint.md) |
