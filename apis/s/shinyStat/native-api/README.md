# ShinyStat: Native API Reference

A consolidated summary of ShinyStat's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.shinystat.com/en/guida.html
- **API base URL:** `https://report.shinystat.com`

## Authentication

### API Key

Use a ShinyStat Tracking ID with API Key and API Secret credentials.

### Credentials

- **API Key:** `apiKey` · required
- **Tracking ID:** `trackingId` · required · Your ShinyStat tracking identifier from Account management > Settings > API Keys.
- **Username:** `username` · required · Your ShinyStat username or customer code, as required by the official Looker Studio integration setup before entering the tracking ID, API key, and API secret.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.shinystat.com/en/guida_integrazione_looker_studio_configurazione.html)

### Session Cookie

Use ShinyStat report credentials to create a cookie-backed session for authenticated report pages.

### Credentials

- **Username:** `username` · required · Your ShinyStat login email.
- **Tracking ID:** `trackingId` · optional · Your ShinyStat tracking ID for the current site.
- **API Key:** `apiKey` · optional · Your ShinyStat API key.

[Official authentication documentation](https://www.shinystat.com/en/guida_integrazione_looker_studio_configurazione.html)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Bounce Rate](actions/get-bounce-rate.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_tasso-di-rimbalzo.html) |
| [Get Summary Dashboard](actions/get-summary-dashboard.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-generale-home.html) |
| [Get Time On Site](actions/get-time-on-site.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-tempi-permanenza.html) |
| [List Average Time On Pages](actions/list-average-time-on-pages.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-tempi-permanenza-media.html) |
| [List Bounce Visits](actions/list-bounce-visits.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_rimbalzi_report.html) |
| [List Country Visits](actions/list-country-visits.md) | `GET` | [docs](https://www.shinystat.com/en/guida_integrazione_looker_studio_creazione_report.html) |
| [List Daily Unique Visitors](actions/list-daily-unique-visitors.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_visitatori-browser-unici-giornalieri.html) |
| [List Landing Pages](actions/list-landing-pages.md) | `GET /pages/enter` | [docs](https://www.shinystat.com/it/guida-elemento_report-pagine-pagine-di-ingresso.html) |
| [List Latest Visits (100/200/500)](actions/list-latest-visits100200500.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-generale-ultime-100-300-visite.html) |
| [List Latest 15 Visits](actions/list-latest15-visits.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-generale-ultime-15-visite.html) |
| [List Monthly Unique Visitors](actions/list-monthly-unique-visitors.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-accessi-visitatori-unici-mensili.html) |
| [List New Visitors](actions/list-new-visitors.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-accessi-nuovi-visitatori.html) |
| [List New Vs Returning Visitors](actions/list-new-vs-returning-visitors.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_Visitatori-nuovi-e-di-ritorno.html) |
| [List Page Views](actions/list-page-views.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-accessi-pagine-viste.html) |
| [List Page Views Per Visit](actions/list-page-views-per-visit.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-pagine-pagine-viste-per-visita.html) |
| [List Requests Per Page](actions/list-requests-per-page.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-pagine-richieste-per-pagine.html) |
| [List Time On Each Page](actions/list-time-on-each-page.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-tempi-permanenza-media-ogni-pagina.html) |
| [List Visit Frequency](actions/list-visit-frequency.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-accessi-frequenza-visita.html) |
| [List Visits](actions/list-visits.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-accessi-visite.html) |
| [List Visits By Hour](actions/list-visits-by-hour.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-accessi-visite-per-ora.html) |
| [List Visits By Week](actions/list-visits-by-week.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_report-accessi-visite-per-settimana.html) |
| [List Weekly Unique Visitors](actions/list-weekly-unique-visitors.md) | `POST /ajax` | [docs](https://www.shinystat.com/it/guida-elemento_visitatori-browser-unici-settimanali.html) |
| [Sign In](actions/sign-in.md) | `POST /login-ex` | [docs](https://www.shinystat.com/en/guida_integrazione_looker_studio_configurazione.html) |
