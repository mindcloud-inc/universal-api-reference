# <img src="https://images.mindcloud.co/apps/icons/g-biz-info_1776356620463.png" alt="gBizINFO logo" width="28" height="28"> gBizINFO: Universal API

Search and monitor Japanese corporate records and filings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gBizINFO/latest
- **Category:** IT Operations / Database
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://info.gbiz.go.jp
- **Vendor API docs:** https://api.info.gbiz.go.jp/hojin/swagger-ui/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company (v2)](actions/get-company-v2.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gBizINFO/latest/actions/get-company-v2?connectionId=$CONNECTION_ID&corporateNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company (v2)](actions/get-company-v2.md) | GET | Retrieves company details from gBizINFO by corporate number. |

