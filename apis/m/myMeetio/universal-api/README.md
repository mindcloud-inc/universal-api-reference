# <img src="https://images.mindcloud.co/apps/icons/my-meetio_1776093920820.png" alt="MyMeet.io logo" width="28" height="28"> MyMeet.io: Universal API

Appointment scheduling and booking platform for managing meeting topics, availability, and public booking pages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/myMeetio/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mymeet.io
- **Vendor API docs:** https://app.mymeet.io/admin/integrations/api/view-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bookings](actions/list-bookings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myMeetio/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET |  |

