# <img src="https://images.mindcloud.co/apps/icons/veteran-confirmation_1777927053668.png" alt="Veteran Confirmation logo" width="28" height="28"> Veteran Confirmation: Universal API

Confirm Title 38 Veteran status with VA

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/veteranConfirmation/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.va.gov/explore/api/veteran-confirmation
- **Vendor API docs:** https://developer.va.gov/explore/api/veteran-confirmation/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Confirm Veteran Status](actions/confirm-veteran-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteranConfirmation/latest/actions/confirm-veteran-status?connectionId=$CONNECTION_ID&firstName=Alfredo&lastName=Armstrong&birthDate=1993-06-08&streetAddressLine1=17020%20Tortoise%20St&city=Round%20Rock&state=TX&zipCode=78664&country=USA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Veteran Status Confirmation

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Veteran Status](actions/confirm-veteran-status.md) | GET |  |

