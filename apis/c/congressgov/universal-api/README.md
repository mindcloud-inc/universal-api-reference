# <img src="https://images.mindcloud.co/apps/icons/congressgov_1776175005404.png" alt="Congress.gov logo" width="28" height="28"> Congress.gov: Universal API

Retrieve congressional legislation, members, committees, and records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/congressgov/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.congress.gov
- **Vendor API docs:** https://github.com/LibraryOfCongress/api.congress.gov

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bills](actions/list-bills.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-bills?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Amendment

| Action | Method | Description |
| --- | --- | --- |
| [Get Amendment](actions/get-amendment.md) | GET | Retrieves an amendment from Congress.gov. |
| [List Amendments](actions/list-amendments.md) | GET | Retrieves amendments from Congress.gov. |

### Amendment Action

| Action | Method | Description |
| --- | --- | --- |
| [List Amendment Actions](actions/list-amendment-actions.md) | GET | Retrieves actions for an amendment from Congress.gov. |

### Amendment Cosponsor

| Action | Method | Description |
| --- | --- | --- |
| [List Amendment Cosponsors](actions/list-amendment-cosponsors.md) | GET | Retrieves cosponsors for an amendment from Congress.gov. |

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Get Bill](actions/get-bill.md) | GET | Retrieves a bill from Congress.gov. |
| [List Bills](actions/list-bills.md) | GET | Retrieves bills from Congress.gov. |
| [List Bills By Congress](actions/list-bills-by-congress.md) | GET | Retrieves bills from a specific Congress in Congress.gov. |
| [List Bills By Congress And Type](actions/list-bills-by-congress-and-type.md) | GET | Retrieves bills by Congress and bill type in Congress.gov. |

### Bill Action

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Actions](actions/list-bill-actions.md) | GET | Retrieves actions for a bill from Congress.gov. |

### Bill Amendment

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Amendments](actions/list-bill-amendments.md) | GET | Retrieves amendments for a bill from Congress.gov. |

### Bill Committee

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Committees](actions/list-bill-committees.md) | GET | Retrieves committees for a bill from Congress.gov. |

### Bill Cosponsor

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Cosponsors](actions/list-bill-cosponsors.md) | GET | Retrieves cosponsors for a bill from Congress.gov. |

### Bill Subject

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Subjects](actions/list-bill-subjects.md) | GET | Retrieves subjects for a bill from Congress.gov. |

### Bill Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Summaries](actions/list-bill-summaries.md) | GET | Retrieves summaries for a bill from Congress.gov. |

### Bill Text Version

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Text Versions](actions/list-bill-text-versions.md) | GET | Retrieves text versions for a bill from Congress.gov. |

### Bill Title

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Titles](actions/list-bill-titles.md) | GET | Retrieves titles for a bill from Congress.gov. |

### Committee

| Action | Method | Description |
| --- | --- | --- |
| [Get Committee](actions/get-committee.md) | GET | Retrieves a committee from Congress.gov. |
| [List Committees](actions/list-committees.md) | GET | Retrieves committees from Congress.gov. |

### Committee Bill

| Action | Method | Description |
| --- | --- | --- |
| [List Committee Bills](actions/list-committee-bills.md) | GET | Retrieves bills for a committee from Congress.gov. |

### Committee Meeting

| Action | Method | Description |
| --- | --- | --- |
| [List Committee Meetings](actions/list-committee-meetings.md) | GET | Retrieves committee meetings from Congress.gov. |

### Committee Print

| Action | Method | Description |
| --- | --- | --- |
| [Get Committee Print](actions/get-committee-print.md) | GET | Retrieves a committee print from Congress.gov. |
| [List Committee Prints](actions/list-committee-prints.md) | GET | Retrieves committee prints from Congress.gov. |

### Committee Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Committee Report](actions/get-committee-report.md) | GET | Retrieves a committee report from Congress.gov. |
| [List Committee Reports](actions/list-committee-reports.md) | GET | Retrieves committee reports from Congress.gov. |

### Congress

| Action | Method | Description |
| --- | --- | --- |
| [Get Congress](actions/get-congress.md) | GET | Retrieves a Congress session from Congress.gov. |
| [Get Current Congress](actions/get-current-congress.md) | GET | Retrieves the current Congress from Congress.gov. |
| [List Congresses](actions/list-congresses.md) | GET | Retrieves Congress sessions from Congress.gov. |

### Hearing

| Action | Method | Description |
| --- | --- | --- |
| [List Hearings](actions/list-hearings.md) | GET | Retrieves hearings from Congress.gov. |

### Law

| Action | Method | Description |
| --- | --- | --- |
| [Get Law](actions/get-law.md) | GET | Retrieves a law from Congress.gov. |
| [List Laws By Congress](actions/list-laws-by-congress.md) | GET | Retrieves laws from a specific Congress in Congress.gov. |
| [List Laws By Congress And Type](actions/list-laws-by-congress-and-type.md) | GET | Retrieves laws by Congress and law type in Congress.gov. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from Congress.gov. |
| [List Members](actions/list-members.md) | GET | Retrieves members from Congress.gov. |
| [List Members By Congress](actions/list-members-by-congress.md) | GET | Retrieves members for a specific Congress in Congress.gov. |

### Member Cosponsored Legislation

| Action | Method | Description |
| --- | --- | --- |
| [List Member Cosponsored Legislation](actions/list-member-cosponsored-legislation.md) | GET | Retrieves legislation cosponsored by a member in Congress.gov. |

### Member Sponsored Legislation

| Action | Method | Description |
| --- | --- | --- |
| [List Member Sponsored Legislation](actions/list-member-sponsored-legislation.md) | GET | Retrieves legislation sponsored by a member in Congress.gov. |

### Related Bill

| Action | Method | Description |
| --- | --- | --- |
| [List Related Bills](actions/list-related-bills.md) | GET | Retrieves related bills for a bill from Congress.gov. |

### Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Summaries](actions/list-summaries.md) | GET | Retrieves bill summaries from Congress.gov. |
| [List Summaries By Congress](actions/list-summaries-by-congress.md) | GET | Retrieves bill summaries from a specific Congress in Congress.gov. |
| [List Summaries By Congress And Bill Type](actions/list-summaries-by-congress-and-bill-type.md) | GET | Retrieves bill summaries by Congress and bill type in Congress.gov. |

