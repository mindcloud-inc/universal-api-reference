# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-04-01-at-18_1775079365788.png" alt="Namsor logo" width="28" height="28"> Namsor: Universal API

Classify personal names by gender, origin, ethnicity, country of residence, and related demographic signals using the Namsor API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/namsor/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://namsor.app
- **Vendor API docs:** https://namsor.app/api-documentation/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Api Status](actions/api-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Api

| Action | Method | Description |
| --- | --- | --- |
| [Api Status](actions/api-status.md) | GET | Retrieves the current Namsor API status. |
| [Api Usage](actions/api-usage.md) | GET | Retrieves current Namsor API usage details. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [Full Name Country](actions/full-name-country.md) | GET | Retrieves the likely country of residence for a full name in Namsor. |
| [Full Name Country Batch](actions/full-name-country-batch.md) | GET | Retrieves likely countries of residence for full names in Namsor. |

### Diaspora

| Action | Method | Description |
| --- | --- | --- |
| [Name Diaspora](actions/name-diaspora.md) | GET | Retrieves the likely diaspora for a name in Namsor by country. |
| [Name Diaspora Batch](actions/name-diaspora-batch.md) | GET | Retrieves likely diasporas for names in Namsor by country. |

### Ethnicity

| Action | Method | Description |
| --- | --- | --- |
| [Name US Race Ethnicity](actions/name-us-race-ethnicity.md) | GET | Retrieves likely US race and ethnicity for a name in Namsor. |
| [Name US Race Ethnicity Batch](actions/name-us-race-ethnicity-batch.md) | GET | Retrieves likely US race and ethnicity for names in Namsor. |
| [Name US Race Ethnicity ZIP5](actions/name-us-race-ethnicity-zip5.md) | GET | Retrieves likely US race and ethnicity for a name in Namsor by ZIP5. |

### Full Name

| Action | Method | Description |
| --- | --- | --- |
| [Genderize Full Name](actions/genderize-full-name.md) | GET | Retrieves the likely gender for a full name in Namsor. |
| [Genderize Full Name Batch](actions/genderize-full-name-batch.md) | GET | Retrieves likely genders for full names in Namsor. |
| [Genderize Full Name Geo](actions/genderize-full-name-geo.md) | GET | Retrieves the likely gender for a full name in Namsor by country. |
| [Genderize Full Name Geo Batch](actions/genderize-full-name-geo-batch.md) | GET | Retrieves likely genders for full names in Namsor by country. |

### Name

| Action | Method | Description |
| --- | --- | --- |
| [Genderize Name](actions/genderize-name.md) | GET | Retrieves the likely gender for a name in Namsor. |
| [Genderize Name Batch](actions/genderize-name-batch.md) | GET | Retrieves likely genders for names in Namsor. |
| [Genderize Name Geo](actions/genderize-name-geo.md) | GET | Retrieves the likely gender for a name in Namsor by country. |
| [Genderize Name Geo Batch](actions/genderize-name-geo-batch.md) | GET | Retrieves likely genders for names in Namsor by country. |
| [Split Name](actions/split-name.md) | GET | Retrieves first and last name parts from a full name in Namsor. |
| [Split Name Batch](actions/split-name-batch.md) | GET | Retrieves first and last name parts for full names in Namsor. |

### Origin

| Action | Method | Description |
| --- | --- | --- |
| [Name Origin](actions/name-origin.md) | GET | Retrieves the likely country of origin for a name in Namsor. |
| [Name Origin Batch](actions/name-origin-batch.md) | GET | Retrieves likely countries of origin for names in Namsor. |

### Phone

| Action | Method | Description |
| --- | --- | --- |
| [Format Phone Number Geo](actions/format-phone-number-geo.md) | GET | Retrieves verified phone number details in Namsor by country. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Available Services](actions/available-services.md) | GET | Retrieves available Namsor API services and credit costs. |

### Software

| Action | Method | Description |
| --- | --- | --- |
| [Software Version](actions/software-version.md) | GET | Retrieves the current Namsor software version. |

