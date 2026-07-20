# <img src="https://images.mindcloud.co/apps/icons/favicon-register-fca-org-uk-48x48_1777914696210.png" alt="FCA logo" width="28" height="28"> FCA: Universal API

Access the UK Financial Conduct Authority Financial Services Register to search firms, individuals, funds, and regulated markets, and retrieve register details such as permissions, requirements, addresses, associated individuals, disciplinary history, passports, waivers, exclusions, and fund subfunds.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fCA/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fca.org.uk/
- **Vendor API docs:** https://register.fca.org.uk/Developer/s/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List regulated markets](actions/list-regulated-markets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fCA/latest/actions/list-regulated-markets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Appointed Representative

| Action | Method | Description |
| --- | --- | --- |
| [List firm appointed representatives](actions/list-firm-appointed-representatives.md) | GET |  |

### Controlled Function

| Action | Method | Description |
| --- | --- | --- |
| [List firm controlled functions](actions/list-firm-controlled-functions.md) | GET |  |

### Firm

| Action | Method | Description |
| --- | --- | --- |
| [Get firm](actions/get-firm.md) | GET |  |
| [Search firms](actions/search-firms.md) | GET |  |

### Firm Address

| Action | Method | Description |
| --- | --- | --- |
| [List firm addresses](actions/list-firm-addresses.md) | GET |  |

### Firm Disciplinary History

| Action | Method | Description |
| --- | --- | --- |
| [List firm disciplinary history](actions/list-firm-disciplinary-history.md) | GET |  |

### Firm Exclusion

| Action | Method | Description |
| --- | --- | --- |
| [List firm exclusions](actions/list-firm-exclusions.md) | GET |  |

### Firm Individual

| Action | Method | Description |
| --- | --- | --- |
| [List firm individuals](actions/list-firm-individuals.md) | GET |  |

### Firm Name

| Action | Method | Description |
| --- | --- | --- |
| [List firm names](actions/list-firm-names.md) | GET |  |

### Firm Passport

| Action | Method | Description |
| --- | --- | --- |
| [List firm passports](actions/list-firm-passports.md) | GET |  |

### Firm Passport Permission

| Action | Method | Description |
| --- | --- | --- |
| [List firm passport permissions](actions/list-firm-passport-permissions.md) | GET |  |

### Firm Permission

| Action | Method | Description |
| --- | --- | --- |
| [List firm permissions](actions/list-firm-permissions.md) | GET |  |

### Firm Regulator

| Action | Method | Description |
| --- | --- | --- |
| [List firm regulators](actions/list-firm-regulators.md) | GET |  |

### Firm Requirement

| Action | Method | Description |
| --- | --- | --- |
| [List firm requirements](actions/list-firm-requirements.md) | GET |  |

### Firm Waiver

| Action | Method | Description |
| --- | --- | --- |
| [List firm waivers](actions/list-firm-waivers.md) | GET |  |

### Fund

| Action | Method | Description |
| --- | --- | --- |
| [Get fund](actions/get-fund.md) | GET |  |
| [Search funds](actions/search-funds.md) | GET |  |

### Fund Name

| Action | Method | Description |
| --- | --- | --- |
| [List fund names](actions/list-fund-names.md) | GET |  |

### Individual

| Action | Method | Description |
| --- | --- | --- |
| [Get individual](actions/get-individual.md) | GET |  |
| [Search individuals](actions/search-individuals.md) | GET |  |

### Individual Controlled Function

| Action | Method | Description |
| --- | --- | --- |
| [List individual controlled functions](actions/list-individual-controlled-functions.md) | GET |  |

### Individual Disciplinary History

| Action | Method | Description |
| --- | --- | --- |
| [List individual disciplinary history](actions/list-individual-disciplinary-history.md) | GET |  |

### Investment Type

| Action | Method | Description |
| --- | --- | --- |
| [List firm requirement investment types](actions/list-firm-requirement-investment-types.md) | GET |  |

### Regulated Market

| Action | Method | Description |
| --- | --- | --- |
| [List regulated markets](actions/list-regulated-markets.md) | GET |  |

### Subfund

| Action | Method | Description |
| --- | --- | --- |
| [List fund subfunds](actions/list-fund-subfunds.md) | GET |  |

