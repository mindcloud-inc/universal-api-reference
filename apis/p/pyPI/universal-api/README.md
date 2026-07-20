# <img src="https://images.mindcloud.co/apps/icons/pypi-icon_1776874815848.png" alt="PyPI logo" width="28" height="28"> PyPI: Universal API

Public read-only integration for the Python Package Index (PyPI), including project metadata, release metadata, file listings, provenance, and registry statistics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pyPI/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pypi.org/
- **Vendor API docs:** https://docs.pypi.org/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get File Provenance](actions/get-file-provenance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-file-provenance?connectionId=$CONNECTION_ID&project=sampleproject&version=4.0.0&filename=sampleproject-4.0.0.tar.gz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get File Provenance](actions/get-file-provenance.md) | GET | Retrieves provenance for a PyPI distribution file. |
| [Get Project Files Index](actions/get-project-files-index.md) | GET | Retrieves distribution download URLs for a PyPI project. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Metadata](actions/get-project-metadata.md) | GET | Retrieves project metadata and release history from PyPI. |

### Releases

| Action | Method | Description |
| --- | --- | --- |
| [Get Release Metadata](actions/get-release-metadata.md) | GET | Retrieves release metadata, ownership, and vulnerabilities from PyPI. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get PyPI Stats](actions/get-py-pi-stats.md) | GET | Retrieves package size statistics from PyPI. |

