# <img src="https://images.mindcloud.co/apps/icons/s-eogpt_1775769563728.png" alt="SEO GPT logo" width="28" height="28"> SEO GPT: Universal API

Generate SEO titles and short-form marketing copy from keywords, brands, and target page URLs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sEOGPT/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seovendor.co/seo-gpt/
- **Vendor API docs:** https://seovendor.co/new-seo-gpt-chrome-plugin-released/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate SEO Title](actions/generate-seo-title.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOGPT/latest/actions/generate-seo-title?connectionId=$CONNECTION_ID&kw=best%20running%20shoes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Generate Article Topic](actions/generate-article-topic.md) | GET |  |
| [Generate Conclusion](actions/generate-conclusion.md) | GET |  |
| [Generate Facebook Post](actions/generate-facebook-post.md) | GET |  |
| [Generate FAQ](actions/generate-faq.md) | GET |  |
| [Generate Feature List](actions/generate-feature-list.md) | GET |  |
| [Generate Google Ad Description](actions/generate-google-ad-description.md) | GET |  |
| [Generate Google Ad Title](actions/generate-google-ad-title.md) | GET |  |
| [Generate H1 Title](actions/generate-h1-title.md) | GET |  |
| [Generate Idea List](actions/generate-idea-list.md) | GET |  |
| [Generate Introduction](actions/generate-introduction.md) | GET |  |
| [Generate Keyword Ideas](actions/generate-keyword-ideas.md) | GET |  |
| [Generate LinkedIn Post](actions/generate-linked-in-post.md) | GET |  |
| [Generate Long-tail Keyword](actions/generate-long-tail-keyword.md) | GET |  |
| [Generate Meta Description](actions/generate-meta-description.md) | GET |  |
| [Generate Product Description](actions/generate-product-description.md) | GET |  |
| [Generate Product Overview](actions/generate-product-overview.md) | GET |  |
| [Generate Product Title](actions/generate-product-title.md) | GET |  |
| [Generate Related Keyword](actions/generate-related-keyword.md) | GET |  |
| [Generate SEO Title](actions/generate-seo-title.md) | GET |  |
| [Generate Twitter Post](actions/generate-twitter-post.md) | GET |  |

