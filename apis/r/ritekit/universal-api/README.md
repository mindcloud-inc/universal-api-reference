# <img src="https://images.mindcloud.co/apps/icons/ritekit_1775769043538.png" alt="Ritekit logo" width="28" height="28"> Ritekit: Universal API

Generate hashtags, emoji suggestions, social-media previews, company logos, and related social publishing assets through the official RiteKit API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ritekit/latest
- **Category:** Marketing / Social Media
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ritekit.com/
- **Vendor API docs:** https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Trending Hashtags](actions/list-trending-hashtags.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/list-trending-hashtags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Extract Article From URL](actions/extract-article-from-url.md) | GET | Extracts article text from a URL with Ritekit. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Brand Colors](actions/get-company-brand-colors.md) | GET | Retrieves company brand colors from Ritekit. |
| [Get Company Logo](actions/get-company-logo.md) | GET | Retrieves a company logo from Ritekit. |
| [Get Domains From Company Name](actions/get-domains-from-company-name.md) | GET | Retrieves likely domains for a company name. |

### Email Insight

| Action | Method | Description |
| --- | --- | --- |
| [Detect Disposable Email](actions/detect-disposable-email.md) | GET | Detects whether an email address is disposable. |
| [Detect Freemail Address](actions/detect-freemail-address.md) | GET | Detects whether an email uses a freemail provider. |
| [Extract Name From Email](actions/extract-name-from-email.md) | GET | Extracts a likely name from an email address. |
| [Get Full Email Insights](actions/get-full-email-insights.md) | GET | Retrieves full email insights from Ritekit. |
| [Suggest Email Typo Fixes](actions/suggest-email-typo-fixes.md) | GET | Retrieves likely typo fixes for an email domain. |

### Emoji

| Action | Method | Description |
| --- | --- | --- |
| [Get Emoji Suggestions](actions/get-emoji-suggestions.md) | GET | Retrieves emoji suggestions from Ritekit for text. |

### Hashtag

| Action | Method | Description |
| --- | --- | --- |
| [Clean Banned Instagram Hashtags](actions/clean-banned-instagram-hashtags.md) | GET | Removes banned Instagram hashtags with Ritekit. |
| [Get Hashtag Stats](actions/get-hashtag-stats.md) | GET | Retrieves real-time stats for Ritekit hashtags. |
| [Get Hashtag Suggestions For Image](actions/get-hashtag-suggestions-for-image.md) | GET | Retrieves Ritekit hashtag suggestions for an image. |
| [Get Hashtag Suggestions For Text](actions/get-hashtag-suggestions-for-text.md) | GET | Retrieves Ritekit hashtag suggestions for text. |
| [Get Hashtag Suggestions For URL](actions/get-hashtag-suggestions-for-url.md) | GET | Retrieves Ritekit hashtag suggestions for a URL. |
| [List Trending Hashtags](actions/list-trending-hashtags.md) | GET | Retrieves trending hashtags from Ritekit. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Extract Top Image From URL](actions/extract-top-image-from-url.md) | GET | Retrieves the top image from a URL with Ritekit. |

### Link Preview

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Preview](actions/get-link-preview.md) | GET | Retrieves a link preview from Ritekit. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Auto-Hashtag Post](actions/auto-hashtag-post.md) | GET | Retrieves auto-hashtagged text from Ritekit. |

### Text

| Action | Method | Description |
| --- | --- | --- |
| [Auto-Emojify Text](actions/auto-emojify-text.md) | GET | Retrieves auto-emojified text from Ritekit. |

