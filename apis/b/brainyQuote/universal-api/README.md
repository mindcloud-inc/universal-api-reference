# <img src="https://images.mindcloud.co/apps/icons/brainy-quote_1776349372738.png" alt="BrainyQuote logo" width="28" height="28"> BrainyQuote: Universal API

Daily quote feeds from BrainyQuote, including today's, art, funny, love, and nature quote feeds.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/brainyQuote/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.brainyquote.com
- **Vendor API docs:** https://www.brainyquote.com/feeds/todays_quote

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Art Quote of the Day](actions/get-art-quote-of-the-day.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brainyQuote/latest/actions/get-art-quote-of-the-day?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Art Quote of the Day](actions/get-art-quote-of-the-day.md) | GET | Retrieves the BrainyQuote art quote of the day feed. |
| [Get Funny Quote of the Day](actions/get-funny-quote-of-the-day.md) | GET | Retrieves the BrainyQuote funny quote of the day feed. |
| [Get Love Quote of the Day](actions/get-love-quote-of-the-day.md) | GET | Retrieves the BrainyQuote love quote of the day feed. |
| [Get Nature Quote of the Day](actions/get-nature-quote-of-the-day.md) | GET | Retrieves the BrainyQuote nature quote of the day feed. |
| [Get Today's Quotes](actions/get-todays-quotes.md) | GET | Retrieves the BrainyQuote quote of the day feed. |

