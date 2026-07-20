# <img src="https://images.mindcloud.co/apps/icons/favicon-api-tophhie-cloud-48x48_1778074107265.png" alt="Tophhie Cloud logo" width="28" height="28"> Tophhie Cloud: Universal API

Public cloud utility APIs for Microsoft Entra tenant information, identifier conversion, domain intelligence, IP checks, generated identifiers, Tophhie Cloud Blog content, and Tophhie Social public statistics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tophhieCloud/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tophhie.cloud
- **Vendor API docs:** https://api.tophhie.cloud

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check IP](actions/check-ip.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/check-ip?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Apple Os Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Apple OS Version](actions/get-apple-os-version.md) | GET | Retrieves the latest Apple OS version for a device in Tophhie Cloud. |

### Blog Author

| Action | Method | Description |
| --- | --- | --- |
| [List Blog Authors](actions/list-blog-authors.md) | GET | Retrieves blog authors from Tophhie Cloud. |

### Blog Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Blog Info](actions/get-blog-info.md) | GET | Retrieves blog information from Tophhie Cloud. |

### Blog Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Blog Post](actions/get-blog-post.md) | GET | Retrieves a blog post from Tophhie Cloud. |
| [List Blog Posts](actions/list-blog-posts.md) | GET | Retrieves blog posts from Tophhie Cloud. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain](actions/get-domain.md) | GET | Retrieves domain details from Tophhie Cloud. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Tophhie Cloud. |

### Entra Id Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Convert Entra ID](actions/convert-entra-id.md) | GET | Converts an Entra ID object ID or SID in Tophhie Cloud. |
| [Convert Entra IDs](actions/convert-entra-ids.md) | GET |  |

### Entra Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Info](actions/get-tenant-info.md) | GET |  |

### Guid

| Action | Method | Description |
| --- | --- | --- |
| [Generate GUIDs](actions/generate-guids.md) | GET | Generates one or more GUIDs in Tophhie Cloud. |

### Ip Check

| Action | Method | Description |
| --- | --- | --- |
| [Check IP](actions/check-ip.md) | GET |  |

### Microsoft 365 Message Center Blog Post

| Action | Method | Description |
| --- | --- | --- |
| [List M365 Message Center Blog Posts](actions/list-m365-message-center-blog-posts.md) | GET | Retrieves Microsoft 365 Message Center blog posts from Tophhie Cloud. |

### Pds Accessibility Score

| Action | Method | Description |
| --- | --- | --- |
| [Get PDS Accessibility Score](actions/get-pds-accessibility-score.md) | GET |  |

### Pds Blob Storage Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get PDS Blob Storage Stats](actions/get-pds-blob-storage-stats.md) | GET | Retrieves PDS blob storage stats from Tophhie Cloud. |

### Pds Blob Storage Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get PDS Blob Storage Usage](actions/get-pds-blob-storage-usage.md) | GET | Retrieves PDS blob storage usage from Tophhie Cloud. |
| [Get PDS Blob Storage Usage By DID](actions/get-pds-blob-storage-usage-by-did.md) | GET | Retrieves PDS blob storage usage by DID from Tophhie Cloud. |

### Pds Bluesky Heatmap

| Action | Method | Description |
| --- | --- | --- |
| [Get PDS Bluesky Heatmap](actions/get-pds-bluesky-heatmap.md) | GET | Retrieves PDS Bluesky heatmap data from Tophhie Cloud. |

### Pds Handle Availability

| Action | Method | Description |
| --- | --- | --- |
| [Verify PDS Handle](actions/verify-pds-handle.md) | GET | Verifies PDS handle availability in Tophhie Cloud. |

### Pds Repository

| Action | Method | Description |
| --- | --- | --- |
| [List PDS Repositories](actions/list-pds-repositories.md) | GET | Retrieves PDS repositories from Tophhie Cloud. |

### Pds Tls Check

| Action | Method | Description |
| --- | --- | --- |
| [Check PDS TLS Domain](actions/check-pds-tls-domain.md) | GET | Verifies PDS TLS eligibility for a domain or handle in Tophhie Cloud. |

### Pds Uptime Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get PDS Uptime Stats](actions/get-pds-uptime-stats.md) | GET | Retrieves PDS uptime statistics from Tophhie Cloud. |

### Redirect

| Action | Method | Description |
| --- | --- | --- |
| [Get Redirect](actions/get-redirect.md) | GET |  |

### Timestamp Ticks

| Action | Method | Description |
| --- | --- | --- |
| [Generate Timestamp Ticks](actions/generate-timestamp-ticks.md) | GET | Retrieves UTC timestamp ticks from Tophhie Cloud. |

