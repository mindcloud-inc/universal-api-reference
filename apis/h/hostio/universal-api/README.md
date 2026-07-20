# Host.io: Universal API

Analyze domains, DNS, related domains, and web metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hostio/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://host.io
- **Vendor API docs:** https://host.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Domain Full Details](actions/get-domain-full-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-full-details?connectionId=$CONNECTION_ID&domain=google.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Domains by AdSense ID](actions/list-domains-by-adsense-id.md) | GET | Finds domains in Host.io by AdSense ID. |
| [List Domains by ASN](actions/list-domains-by-asn.md) | GET | Finds domains in Host.io by ASN. |
| [List Domains by Backlink Target](actions/list-domains-by-backlink-target.md) | GET | Finds domains in Host.io by backlink target. |
| [List Domains by Email Address](actions/list-domains-by-email-address.md) | GET | Finds domains in Host.io by email address. |
| [List Domains by Facebook Handle](actions/list-domains-by-facebook-handle.md) | GET | Finds domains in Host.io by Facebook handle. |
| [List Domains by Google Analytics ID](actions/list-domains-by-google-analytics-id.md) | GET | Finds domains in Host.io by Google Analytics ID. |
| [List Domains by Google Tag Manager ID](actions/list-domains-by-google-tag-manager-id.md) | GET | Finds domains in Host.io by Google Tag Manager ID. |
| [List Domains by Instagram Handle](actions/list-domains-by-instagram-handle.md) | GET | Finds domains in Host.io by Instagram handle. |
| [List Domains by IP Address](actions/list-domains-by-ip-address.md) | GET | Finds domains in Host.io by IP address. |
| [List Domains by Mail Server](actions/list-domains-by-mail-server.md) | GET | Finds domains in Host.io by mail server. |
| [List Domains by Name Server](actions/list-domains-by-name-server.md) | GET | Finds domains in Host.io by name server. |
| [List Domains by Redirect Target](actions/list-domains-by-redirect-target.md) | GET | Finds domains in Host.io by redirect target. |
| [List Domains by Twitter Handle](actions/list-domains-by-twitter-handle.md) | GET | Finds domains in Host.io by Twitter handle. |

### Domain Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Full Details](actions/get-domain-full-details.md) | GET | Retrieves full domain details from Host.io. |

### Domain Dns Records

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain DNS Records](actions/get-domain-dns-records.md) | GET | Retrieves DNS records for a domain from Host.io. |

### Domain Web Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Web Metadata](actions/get-domain-web-metadata.md) | GET | Retrieves web metadata for a domain from Host.io. |

### Related Domain Counts

| Action | Method | Description |
| --- | --- | --- |
| [Get Related Domain Counts](actions/get-related-domain-counts.md) | GET | Retrieves related domain counts from Host.io. |

