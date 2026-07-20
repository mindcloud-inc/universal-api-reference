# <img src="https://images.mindcloud.co/apps/icons/booth-book_1774628832644.png" alt="BoothBook logo" width="28" height="28"> BoothBook: Universal API

BoothBook is an event-booking platform for booth and event businesses. This draft wrapper exposes the currently documented BoothBook developer API for account and booking reads and remains blocked on live BoothBook API ingress verification.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/boothBook/latest
- **Category:** Commerce
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://boothbook.com/
- **Vendor API docs:** https://v1-support.boothbook.com/article/developer-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from BoothBook. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from BoothBook. |

