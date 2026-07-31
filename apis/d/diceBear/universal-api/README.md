# <img src="https://images.mindcloud.co/apps/icons/dice-bear_1777576244258.png" alt="DiceBear logo" width="28" height="28"> DiceBear: Universal API

Generate DiceBear 10.x avatars. Public API use is non-commercial; SVG is 50 rps and raster is 10 rps. Commercial or higher-volume use requires self-hosting or provider confirmation; styles have individual licenses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/diceBear/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dicebear.com/
- **Vendor API docs:** https://www.dicebear.com/how-to-use/http-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Avatar Metadata](actions/get-avatar-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/get-avatar-metadata?connectionId=$CONNECTION_ID&styleName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Avatar

| Action | Method | Description |
| --- | --- | --- |
| [Generate Adventurer Avatar](actions/generate-adventurer-avatar.md) | GET |  |
| [Generate Adventurer Neutral Avatar](actions/generate-adventurer-neutral-avatar.md) | GET |  |
| [Generate Avataaars Avatar](actions/generate-avataaars-avatar.md) | GET |  |
| [Generate Avataaars Neutral Avatar](actions/generate-avataaars-neutral-avatar.md) | GET |  |
| [Generate Avatar Image](actions/generate-avatar-image.md) | GET |  |
| [Generate Bottts Avatar](actions/generate-bottts-avatar.md) | GET |  |
| [Generate Bottts Neutral Avatar](actions/generate-bottts-neutral-avatar.md) | GET |  |
| [Generate Icons Avatar](actions/generate-icons-avatar.md) | GET |  |
| [Generate Identicon Avatar](actions/generate-identicon-avatar.md) | GET |  |
| [Generate Initials Avatar](actions/generate-initials-avatar.md) | GET |  |
| [Generate Lorelei Avatar](actions/generate-lorelei-avatar.md) | GET |  |
| [Generate Lorelei Neutral Avatar](actions/generate-lorelei-neutral-avatar.md) | GET |  |
| [Generate Open Peeps Avatar](actions/generate-open-peeps-avatar.md) | GET |  |
| [Generate Personas Avatar](actions/generate-personas-avatar.md) | GET |  |
| [Generate Pixel Art Avatar](actions/generate-pixel-art-avatar.md) | GET |  |
| [Generate Pixel Art Neutral Avatar](actions/generate-pixel-art-neutral-avatar.md) | GET |  |
| [Generate Rings Avatar](actions/generate-rings-avatar.md) | GET |  |
| [Generate Shapes Avatar](actions/generate-shapes-avatar.md) | GET |  |
| [Generate Thumbs Avatar](actions/generate-thumbs-avatar.md) | GET |  |

### Avatar Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Avatar Metadata](actions/get-avatar-metadata.md) | GET |  |

### Avatar Style Catalog

| Action | Method | Description |
| --- | --- | --- |
| [List Avatar Styles](actions/list-avatar-styles.md) | GET |  |

### Avatar Style Options

| Action | Method | Description |
| --- | --- | --- |
| [Get Style Options](actions/get-style-options.md) | GET |  |

### Style Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Style Definition](actions/get-style-definition.md) | GET |  |

