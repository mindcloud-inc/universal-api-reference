# <img src="https://images.mindcloud.co/apps/icons/favicon-4_1775817987722.png" alt="Scrape Creators logo" width="28" height="28"> Scrape Creators: Universal API

Scrape social media profiles, videos, ads, and creator data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapeCreators/latest
- **Category:** Marketing / Social Media
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrapecreators.com
- **Vendor API docs:** https://docs.scrapecreators.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves your Scrape Creators credit balance. |

### Facebook Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Facebook Profile](actions/get-facebook-profile.md) | GET | Retrieves a Facebook profile from Scrape Creators. |

### Google Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Google Search Results](actions/get-google-search-results.md) | GET | Retrieves Google search results from Scrape Creators. |

### Instagram Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Instagram Basic Profile](actions/get-instagram-basic-profile.md) | GET | Retrieves an Instagram basic profile from Scrape Creators. |

### Linkedin Company

| Action | Method | Description |
| --- | --- | --- |
| [Get LinkedIn Company Page](actions/get-linked-in-company-page.md) | GET | Retrieves a LinkedIn company page from Scrape Creators. |

### Linkedin Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get LinkedIn Profile](actions/get-linked-in-profile.md) | GET | Retrieves a LinkedIn profile from Scrape Creators. |

### Linkme Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Linkme Profile](actions/get-linkme-profile.md) | GET | Retrieves a Linkme profile by URL from Scrape Creators. |

### Linktree Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Linktree Page](actions/get-linktree-page.md) | GET | Retrieves a Linktree page from Scrape Creators. |

### Snapchat Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Snapchat User Profile](actions/get-snapchat-user-profile.md) | GET | Retrieves a Snapchat user profile from Scrape Creators. |

### Threads Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Threads Profile](actions/get-threads-profile.md) | GET | Retrieves a Threads profile from Scrape Creators. |

### Tiktok Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get TikTok Profile](actions/get-tik-tok-profile.md) | GET | Retrieves a TikTok profile from Scrape Creators. |

### Tiktok Song

| Action | Method | Description |
| --- | --- | --- |
| [Get TikTok Song Details](actions/get-tik-tok-song-details.md) | GET | Retrieves TikTok song details from Scrape Creators. |

### Tiktok Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get TikTok Transcript](actions/get-tik-tok-transcript.md) | GET | Retrieves a TikTok video transcript from Scrape Creators. |

### Tiktok Trending Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get TikTok Trending Feed](actions/get-tik-tok-trending-feed.md) | GET | Retrieves TikTok trending feed items from Scrape Creators. |

### Tiktok Video

| Action | Method | Description |
| --- | --- | --- |
| [Get TikTok Video Info](actions/get-tik-tok-video-info.md) | GET | Retrieves TikTok video details from Scrape Creators. |

### Twitter Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Twitter Profile](actions/get-twitter-profile.md) | GET | Retrieves a Twitter profile from Scrape Creators. |

### Youtube Short

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Trending Shorts](actions/get-you-tube-trending-shorts.md) | GET | Retrieves trending YouTube Shorts from Scrape Creators. |

### Youtube Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Transcript](actions/get-you-tube-transcript.md) | GET | Retrieves a YouTube video transcript from Scrape Creators. |

### Youtube Video

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Video Details](actions/get-you-tube-video-details.md) | GET | Retrieves YouTube video or Short details from Scrape Creators. |

