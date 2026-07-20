# <img src="https://images.mindcloud.co/apps/icons/favicon-www-hopewiser-com-48x48_1777039118789.png" alt="Hopewiser logo" width="28" height="28"> Hopewiser: Universal API

Hopewiser provides cloud address lookup and validation APIs for UK and international address data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hopewiser/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hopewiser.com
- **Vendor API docs:** https://www.hopewiser.com/developer-document/developer-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Master Address Files](actions/list-master-address-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/list-master-address-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Address Output Field

| Action | Method | Description |
| --- | --- | --- |
| [List UK Address Output Fields](actions/list-uk-address-output-fields.md) | GET |  |

### Address Search Index

| Action | Method | Description |
| --- | --- | --- |
| [List UK Address Search Indexes](actions/list-uk-address-search-indexes.md) | GET |  |

### Address Service Version

| Action | Method | Description |
| --- | --- | --- |
| [Get UK Address Service Versions](actions/get-uk-address-service-versions.md) | GET |  |

### Autocomplete Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Autocomplete UK Address By SID](actions/get-autocomplete-uk-address-by-sid.md) | GET |  |

### Autocomplete Address Result

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete UK Address](actions/autocomplete-uk-address.md) | GET |  |

### Autocomplete Master Address File

| Action | Method | Description |
| --- | --- | --- |
| [List Autocomplete Master Address Files](actions/list-autocomplete-master-address-files.md) | GET |  |

### Autocomplete Output Field

| Action | Method | Description |
| --- | --- | --- |
| [List Autocomplete Output Fields](actions/list-autocomplete-output-fields.md) | GET |  |

### Autocomplete Service Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Autocomplete Service Versions](actions/get-autocomplete-service-versions.md) | GET |  |

### International Country

| Action | Method | Description |
| --- | --- | --- |
| [List International Countries](actions/list-international-countries.md) | GET |  |

### Master Address File

| Action | Method | Description |
| --- | --- | --- |
| [List Master Address Files](actions/list-master-address-files.md) | GET |  |

### Uk Address

| Action | Method | Description |
| --- | --- | --- |
| [Get UK Address By SID](actions/get-uk-address-by-sid.md) | GET |  |

### Uk Address Result

| Action | Method | Description |
| --- | --- | --- |
| [Search UK Address](actions/search-uk-address.md) | GET |  |

