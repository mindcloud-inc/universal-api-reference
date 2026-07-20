# <img src="https://images.mindcloud.co/apps/icons/uplink_1776436170675.png" alt="myUplink logo" width="28" height="28"> myUplink: Universal API

Control and monitor myUplink-connected heating and indoor climate systems through the myUplink public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/myUplink/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://myuplink.com
- **Vendor API docs:** https://dev.myuplink.com/documentation/intro?activeTab=intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authorized API Availability](actions/test-authorized-api-availability.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myUplink/latest/actions/test-authorized-api-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Test API Availability](actions/test-api-availability.md) | GET | Tests public API availability in myUplink. |
| [Test Authorized API Availability](actions/test-authorized-api-availability.md) | GET | Tests authorized API availability in myUplink. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get My Systems](actions/get-my-systems.md) | GET | Retrieves systems for the authenticated myUplink user. |

