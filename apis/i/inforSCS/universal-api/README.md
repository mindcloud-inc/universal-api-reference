# <img src="https://images.mindcloud.co/apps/icons/infor-reserve-cloud-scs_1782742973395.png" alt="Infor ReserveCloud SCS logo" width="28" height="28"> Infor ReserveCloud SCS: Universal API

Infor ReserveCloud SCS through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/inforSCS/latest
- **Category:** Commerce / ERP
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.reservecloud.com/web/university/universityDocumentDownloadViewable/50066

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inforSCS/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Event Services](actions/list-event-services.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |
| [List Functions](actions/list-functions.md) | GET |  |
| [List Transaction](actions/list-transaction.md) | GET |  |

