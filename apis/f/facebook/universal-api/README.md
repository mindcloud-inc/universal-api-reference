# <img src="https://images.mindcloud.co/apps/icons/facebook_1782742775472.png" alt="Facebook logo" width="28" height="28"> Facebook: Universal API

Connect Facebook Pages, Meta Business assets, and advertising data to workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/facebook/latest
- **Category:** Marketing / Social Media
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.facebook.com/business
- **Vendor API docs:** https://developers.facebook.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pages](actions/list-pages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/list-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Ad Accounts](actions/list-ad-accounts.md) | GET | Retrieve a list of the advertising accounts to which the authenticated user has access. |
| [List Businesses](actions/list-businesses.md) | GET | Retrieve a list of the business accounts to which the authenticated user has access. |

### Ad Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Ad Campaign Query](actions/ad-campaign-query.md) | GET |  |

### Ads

| Action | Method | Description |
| --- | --- | --- |
| [Ad Account Ads Query](actions/ad-account-ads-query.md) | GET |  |
| [List Daily Ad Insights](actions/list-daily-ad-insights.md) | GET | Retrieves daily spend, clicks, and conversion events for Meta ads. |

### Instagram Media

| Action | Method | Description |
| --- | --- | --- |
| [Publish Instagram Media](actions/publish-instagram-media.md) | POST |  |

### Instagram Media Container

| Action | Method | Description |
| --- | --- | --- |
| [Create Instagram Carousel Container](actions/create-instagram-carousel-container.md) | POST |  |
| [Create Instagram Image Container](actions/create-instagram-image-container.md) | POST |  |
| [Create Instagram Image Story Container](actions/create-instagram-image-story-container.md) | POST |  |
| [Create Instagram Resumable Reel Container](actions/create-instagram-resumable-reel-container.md) | POST |  |
| [Get Instagram Container Status](actions/get-instagram-container-status.md) | GET |  |
| [Upload Instagram Container Video](actions/upload-instagram-container-video.md) | POST |  |

### Instagram Publishing Quota

| Action | Method | Description |
| --- | --- | --- |
| [Get Instagram Publishing Limit](actions/get-instagram-publishing-limit.md) | GET |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET | List pages you manage/own |

### Page Photo

| Action | Method | Description |
| --- | --- | --- |
| [Create Page Photo](actions/create-page-photo.md) | POST |  |

### Page Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Page Post](actions/create-page-post.md) | POST |  |

### Page Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Page Video](actions/create-page-video.md) | POST |  |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Owned Pages](actions/get-owned-pages.md) | GET | Retrieve a list of Pages owned by the specified business account. |
| [Get Page Insights](actions/get-page-insights.md) | GET | Get analytics and metrics for a Page. |

