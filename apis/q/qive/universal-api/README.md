# <img src="https://images.mindcloud.co/apps/icons/qive_1776776070955.png" alt="Qive logo" width="28" height="28"> Qive: Universal API

Qive is a Brazilian fiscal document automation API for retrieving, uploading, and managing electronic fiscal documents such as NF-e, NFS-e, CT-e, invoices, and related events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qive/latest
- **Category:** Commerce / Accounting
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://qive.com.br/
- **Vendor API docs:** https://developers.qive.com.br/docs/get/v1/nfe/received

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Companies](actions/get-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Companies](actions/get-companies.md) | GET |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Properties](actions/list-properties.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Authorized CTes](actions/list-authorized-ctes.md) | GET |  |
| [List Authorized NFes](actions/list-authorized-nfes.md) | GET |  |
| [List Emitted NFes](actions/list-emitted-nfes.md) | GET |  |
| [List Emitted NFSes](actions/list-emitted-nfses.md) | GET |  |
| [List NFe Manifests](actions/list-nfe-manifests.md) | GET |  |
| [List NFe Manifests V2](actions/list-nfe-manifests-v2.md) | GET |  |
| [List Not-Taker CTe-OS](actions/list-not-taker-cte-os.md) | GET |  |
| [List Not-Taker CTes](actions/list-not-taker-ctes.md) | GET |  |
| [List Received NFes](actions/list-received-nfes.md) | GET |  |
| [List Received NFSes](actions/list-received-nfses.md) | GET |  |
| [List Received NFSes V2](actions/list-received-nfses-v2.md) | GET |  |
| [List Taker CTe-OS](actions/list-taker-cte-os.md) | GET |  |
| [List Taker CTes](actions/list-taker-ctes.md) | GET |  |
| [List Transporter NFes](actions/list-transporter-nfes.md) | GET |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List CTe Events](actions/list-cte-events.md) | GET |  |
| [List CTe Events V2](actions/list-cte-events-v2.md) | GET |  |
| [List CTe-OS Events](actions/list-cte-os-events.md) | GET |  |
| [List NFe Events V2](actions/list-nfe-events-v2.md) | GET |  |
| [List NFSe Events](actions/list-nfse-events.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get DACTe](actions/get-dacte.md) | GET |  |
| [Get DACTe-OS](actions/get-dacte-os.md) | GET |  |
| [Get DANFe](actions/get-danfe.md) | GET |  |
| [Get DANFSe](actions/get-danfse.md) | GET |  |
| [Get Emitted NFSe Manual PDF](actions/get-emitted-nfse-manual-pdf.md) | GET |  |
| [Get Received NFSe Manual PDF](actions/get-received-nfse-manual-pdf.md) | GET |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get CTe Upload Status](actions/get-cte-upload-status.md) | GET |  |
| [Get NFe Manifest Status](actions/get-nfe-manifest-status.md) | GET |  |
| [Get NFe Upload Status](actions/get-nfe-upload-status.md) | GET |  |

