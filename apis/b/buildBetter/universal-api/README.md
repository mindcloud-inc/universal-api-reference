# <img src="https://images.mindcloud.co/apps/icons/build-better_1774878203072.png" alt="BuildBetter logo" width="28" height="28"> BuildBetter: Universal API

Query calls, signals, people, companies, and documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/buildBetter/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://buildbetter.ai
- **Vendor API docs:** https://docs.buildbetter.ai/pages/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Recent Calls](actions/list-recent-calls.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-recent-calls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call By ID](actions/get-call-by-id.md) | GET |  |
| [Get Call Details With Participants](actions/get-call-details-with-participants.md) | GET |  |
| [Get Call Transcript](actions/get-call-transcript.md) | GET |  |
| [List Calls by Date Range](actions/list-calls-by-date-range.md) | GET |  |
| [List Calls by Participant Email](actions/list-calls-by-participant-email.md) | GET |  |
| [List Calls Paginated](actions/list-calls-paginated.md) | GET |  |
| [List Recent Calls](actions/list-recent-calls.md) | GET |  |
| [Search Calls By Title](actions/search-calls-by-title.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Get Company By ID](actions/get-company-by-id.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Search Companies By Name Or Domain](actions/search-companies-by-name-or-domain.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST |  |
| [Get Person By ID](actions/get-person-by-id.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |
| [List People by Company](actions/list-people-by-company.md) | GET |  |
| [Search People By Name](actions/search-people-by-name.md) | GET |  |
| [Update Person](actions/update-person.md) | PUT |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List Conversations](actions/list-conversations.md) | GET |  |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Signal By ID](actions/get-signal-by-id.md) | GET |  |
| [List Recent Signals](actions/list-recent-signals.md) | GET |  |
| [List Signals by Date Range](actions/list-signals-by-date-range.md) | GET |  |
| [List Signals by Sentiment](actions/list-signals-by-sentiment.md) | GET |  |
| [List Signals by Type](actions/list-signals-by-type.md) | GET |  |
| [List Signals for Call](actions/list-signals-for-call.md) | GET |  |
| [Search Signals By Summary Phrase](actions/search-signals-by-summary-phrase.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Document By ID](actions/get-document-by-id.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET |  |

