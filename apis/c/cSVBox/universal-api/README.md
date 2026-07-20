# <img src="https://images.mindcloud.co/apps/icons/csvbox-logo_1781649270692.png" alt="CSVBox logo" width="28" height="28"> CSVBox: Universal API

Import CSV and spreadsheet data into your app with embeddable CSVBox importers and automated destination delivery.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cSVBox/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://csvbox.io/
- **Vendor API docs:** https://help.csvbox.io/advanced-installation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Connection](actions/verify-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Connected User

| Action | Method | Description |
| --- | --- | --- |
| [Verify Connection](actions/verify-connection.md) | GET |  |

### Import Job

| Action | Method | Description |
| --- | --- | --- |
| [Submit File From Public URL](actions/submit-file-from-public-url.md) | POST |  |
| [Upload File](actions/upload-file.md) | POST |  |

