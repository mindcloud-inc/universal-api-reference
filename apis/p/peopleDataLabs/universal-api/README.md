# <img src="https://images.mindcloud.co/apps/icons/people-data-labs_1774041909455.png" alt="People Data Labs logo" width="28" height="28"> People Data Labs: Universal API

Enrich person, company, and IP data with People Data Labs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peopleDataLabs/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.peopledatalabs.com/
- **Vendor API docs:** https://docs.peopledatalabs.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Clean Location](actions/clean-location.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-location?connectionId=$CONNECTION_ID&location=san%20francisco%2C%20california%2C%20united%20states" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Autocomplete Result

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete](actions/autocomplete.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Enrich Companies](actions/bulk-enrich-companies.md) | GET |  |
| [Clean Company](actions/clean-company.md) | GET |  |
| [Enrich Company](actions/enrich-company.md) | GET |  |
| [Search Companies](actions/search-companies.md) | GET |  |

### Ip

| Action | Method | Description |
| --- | --- | --- |
| [Enrich IP](actions/enrich-ip.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Clean Location](actions/clean-location.md) | GET |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Enrich People](actions/bulk-enrich-people.md) | GET |  |
| [Enrich Person](actions/enrich-person.md) | GET |  |
| [Search People](actions/search-people.md) | GET |  |

### School

| Action | Method | Description |
| --- | --- | --- |
| [Clean School](actions/clean-school.md) | GET |  |

