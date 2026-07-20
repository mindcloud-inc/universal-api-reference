# <img src="https://images.mindcloud.co/apps/icons/bitly_1773245973497.png" alt="Bitly logo" width="28" height="28"> Bitly: Universal API

Shorten, manage, and analyze Bitly links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bitly/latest
- **Category:** Marketing
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bitly.com
- **Vendor API docs:** https://dev.bitly.com/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Expand Bitlink](actions/expand-bitlink.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/expand-bitlink?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Bitlink

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Group Bitlinks](actions/bulk-update-group-bitlinks.md) | PUT | Updates tags or archives multiple group bitlinks in Bitly. |
| [Delete Bitlink](actions/delete-bitlink.md) | DELETE | Deletes an unedited hash bitlink from Bitly. |
| [Expand Bitlink](actions/expand-bitlink.md) | GET | Retrieves the long URL for a Bitly bitlink. |
| [Get Bitlink](actions/get-bitlink.md) | GET | Retrieves a bitlink from your Bitly account. |
| [Get Sorted Bitlinks](actions/get-sorted-bitlinks.md) | GET | Retrieves sorted bitlinks for a group in Bitly. |
| [List Group Bitlinks](actions/list-group-bitlinks.md) | GET | Retrieves bitlinks for a group in Bitly. |
| [Shorten Link](actions/shorten-link.md) | POST | Creates a shortened link in Bitly. |

### Bsd

| Action | Method | Description |
| --- | --- | --- |
| [List BSDs](actions/list-bsds.md) | GET | Retrieves branded short domains from Bitly. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from your Bitly account. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from your Bitly account. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Bitly. |

### Group Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Preferences](actions/get-group-preferences.md) | GET | Retrieves group preferences from your Bitly account. |
| [Update Group Preferences](actions/update-group-preferences.md) | PUT | Updates existing group preferences in Bitly. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from your Bitly account. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from your Bitly account. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Full Bitlink](actions/create-full-bitlink.md) | POST | Creates a bitlink in Bitly with additional parameters. |
| [Get Group Feature Usage](actions/get-group-feature-usage.md) | GET | Retrieves feature usage for a Bitly group. |
| [Get OAuth App](actions/get-oauth-app.md) | GET | Retrieves an OAuth app from Bitly. |
| [Get Organization Shorten Counts By Group](actions/get-organization-shorten-counts-by-group.md) | GET | Retrieves organization shorten counts by group in Bitly. |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code from Bitly. |
| [Get QR Code Image](actions/get-qr-code-image.md) | GET | Retrieves a QR code image from Bitly. |
| [List Group QR Codes](actions/list-group-qr-codes.md) | GET | Retrieves QR codes for a group in Bitly. |
| [Update Bitlink](actions/update-bitlink.md) | PUT | Updates an existing bitlink in Bitly. |
| [Update QR Code](actions/update-qr-code.md) | PUT | Updates an existing QR code in Bitly. |

### Plan Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Plan Limits](actions/get-organization-plan-limits.md) | GET | Retrieves organization plan limits from Bitly. |

### Platform Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get Platform Limits](actions/get-platform-limits.md) | GET | Retrieves platform limits from your Bitly account. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Group Tags](actions/list-group-tags.md) | GET | Retrieves tags for a group in Bitly. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the current authenticated Bitly user. |

