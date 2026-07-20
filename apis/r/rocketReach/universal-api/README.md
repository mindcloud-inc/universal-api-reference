# <img src="https://images.mindcloud.co/apps/icons/rocket-reach_1773695257807.png" alt="RocketReach logo" width="28" height="28"> RocketReach: Universal API

Search people, companies, and contact data with RocketReach

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rocketReach/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rocketreach.co
- **Vendor API docs:** https://docs.rocketreach.co/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Person Lookup Status](actions/check-person-lookup-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/check-person-lookup-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from RocketReach. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a RocketReach API key. |

### Bulk Person Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Lookup Universal People](actions/bulk-lookup-universal-people.md) | POST | Creates a RocketReach Universal bulk people lookup. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Company](actions/lookup-company.md) | GET | Retrieves a company from RocketReach. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in RocketReach. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Universal Company](actions/lookup-universal-company.md) | GET | Retrieves a company from RocketReach Universal lookup. |
| [Search Universal Companies](actions/search-universal-companies.md) | GET | Finds companies in RocketReach Universal search. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Lookup People](actions/bulk-lookup-people.md) | POST | Creates a RocketReach bulk people lookup. |
| [Check Person Lookup Status](actions/check-person-lookup-status.md) | GET | Retrieves person lookup status from RocketReach. |
| [Lookup Person](actions/lookup-person.md) | GET | Retrieves a person from RocketReach. |
| [Lookup Universal Person](actions/lookup-universal-person.md) | GET | Retrieves a person from RocketReach Universal lookup. |
| [Search People](actions/search-people.md) | GET | Finds people in RocketReach. |
| [Search Universal People](actions/search-universal-people.md) | GET | Finds people in RocketReach Universal search. |

### Person And Company

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Person And Company](actions/lookup-person-and-company.md) | GET | Retrieves a person and company from RocketReach. |

### Person Lookup Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Universal Person Lookup Status](actions/check-universal-person-lookup-status.md) | GET | Retrieves Universal person lookup status from RocketReach. |

### Universal Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Universal Account](actions/get-universal-account.md) | GET | Retrieves universal account details from RocketReach. |

