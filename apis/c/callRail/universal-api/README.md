# <img src="https://images.mindcloud.co/apps/icons/call-rail_1773337643077.png" alt="CallRail logo" width="28" height="28"> CallRail: Universal API

CallRail provides call tracking, form tracking, lead attribution, and conversation intelligence for marketers and agencies.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/callRail/latest
- **Category:** Marketing
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.callrail.com
- **Vendor API docs:** https://apidocs.callrail.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from CallRail. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from CallRail. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from CallRail. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from CallRail. |
| [Update Call](actions/update-call.md) | PUT | Updates a call in CallRail. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a company in CallRail. |
| [Disable Company](actions/disable-company.md) | DELETE | Disables a company in CallRail. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from CallRail. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from CallRail. |
| [Update Company](actions/update-company.md) | PUT | Updates a company in CallRail. |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Submission](actions/create-form-submission.md) | POST | Creates a form submission in CallRail. |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves form submissions from CallRail. |
| [Update Form Submission](actions/update-form-submission.md) | PUT | Updates a form submission in CallRail. |

### Page View

| Action | Method | Description |
| --- | --- | --- |
| [List Call Page Views](actions/list-call-page-views.md) | GET | Retrieves page views for a CallRail call. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Recording](actions/get-call-recording.md) | GET | Retrieves a call recording from CallRail. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Call Data](actions/summarize-call-data.md) | GET | Retrieves call summary data from CallRail. |
| [Summarize Call Data By Time Series](actions/summarize-call-data-by-time-series.md) | GET | Retrieves call time-series summary data from CallRail. |
| [Summarize Form Data](actions/summarize-form-data.md) | GET | Retrieves form summary data from CallRail. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a tag in CallRail. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from CallRail. |
| [Remove Tag](actions/remove-tag.md) | DELETE | Deletes a tag from CallRail. |
| [Update Tag](actions/update-tag.md) | PUT | Updates a tag in CallRail. |

