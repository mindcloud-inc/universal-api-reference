# <img src="https://images.mindcloud.co/apps/icons/addressfinder_1774887374936.png" alt="Addressfinder logo" width="28" height="28"> Addressfinder: Universal API

Verify addresses, locations, emails, and phone numbers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/addressfinder/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://addressfinder.com
- **Vendor API docs:** https://addressfinder.com/au/docs/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List AU Address Suggestions](actions/list-au-address-suggestions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-address-suggestions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Get AU Address Metadata](actions/get-au-address-metadata.md) | GET | Retrieves metadata for an Australian address from Addressfinder. |
| [List AU Address Suggestions](actions/list-au-address-suggestions.md) | GET | Finds Australian address suggestions in Addressfinder by partial query. |
| [Verify AU Address](actions/verify-au-address.md) | GET | Verifies a full Australian address in Addressfinder. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get AU Location Metadata](actions/get-au-location-metadata.md) | GET | Retrieves metadata for an Australian location from Addressfinder. |
| [List AU Location Suggestions](actions/list-au-location-suggestions.md) | GET | Finds Australian location suggestions in Addressfinder by partial query. |

