# <img src="https://images.mindcloud.co/apps/icons/redirectpizza_1774887212632.png" alt="redirect.pizza logo" width="28" height="28"> redirect.pizza: Universal API

Manage redirects, email forwards, domains, and traffic analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/redirectpizza/latest
- **Category:** Marketing
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://redirect.pizza/
- **Vendor API docs:** https://redirect.pizza/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Team Details](actions/get-team-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-team-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Dimension](actions/get-analytics-dimension.md) | GET |  |
| [Get Analytics Hits](actions/get-analytics-hits.md) | GET |  |
| [Get Analytics Raw Hits](actions/get-analytics-raw-hits.md) | GET |  |
| [Get Analytics Time Series](actions/get-analytics-time-series.md) | GET |  |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Apply Automatic DNS](actions/apply-automatic-dns.md) | PUT |  |
| [Check Domain DNS](actions/check-domain-dns.md) | PUT |  |
| [Get Domain](actions/get-domain.md) | GET |  |
| [List Domains](actions/list-domains.md) | GET |  |

### Email Forward

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Forward](actions/create-email-forward.md) | POST |  |
| [Delete Email Forward](actions/delete-email-forward.md) | DELETE |  |
| [Get Email Forward](actions/get-email-forward.md) | GET |  |
| [List Email Forwards](actions/list-email-forwards.md) | GET |  |
| [Update Email Forward](actions/update-email-forward.md) | PUT |  |

### Redirect

| Action | Method | Description |
| --- | --- | --- |
| [Create Redirect](actions/create-redirect.md) | POST |  |
| [Delete Redirect](actions/delete-redirect.md) | DELETE |  |
| [Get Redirect](actions/get-redirect.md) | GET |  |
| [List Redirects](actions/list-redirects.md) | GET |  |
| [Update Redirect](actions/update-redirect.md) | PUT |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Details](actions/get-team-details.md) | GET |  |

### Utility

| Action | Method | Description |
| --- | --- | --- |
| [Generate QR Code](actions/generate-qr-code.md) | GET |  |
| [Test Redirects](actions/test-redirects.md) | GET |  |

