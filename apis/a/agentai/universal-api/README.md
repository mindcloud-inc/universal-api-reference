# <img src="https://images.mindcloud.co/apps/icons/agentai_1775849112783.png" alt="Agent.ai logo" width="28" height="28"> Agent.ai: Universal API

Research the web, enrich data, and generate AI outputs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agentai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://agent.ai
- **Vendor API docs:** https://docs.agent.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Web Page Content](actions/get-web-page-content.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-web-page-content?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agent Run

| Action | Method | Description |
| --- | --- | --- |
| [Invoke Agent](actions/invoke-agent.md) | POST | Invokes an agent in Agent.ai with input or a prompt. |

### Ai Response

| Action | Method | Description |
| --- | --- | --- |
| [Use GenAI](actions/use-genai.md) | POST | Creates AI-generated text in Agent.ai from instructions. |

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Convert Text To Speech](actions/convert-text-to-speech.md) | POST | Creates a speech audio file from text in Agent.ai. |

### Bluesky Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Bluesky Posts](actions/get-bluesky-posts.md) | GET | Retrieves Bluesky posts from Agent.ai by handle. |
| [Search Bluesky Posts](actions/search-bluesky-posts.md) | GET | Finds Bluesky posts in Agent.ai by query. |

### Company Data

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Company Data](actions/enrich-company-data.md) | GET | Retrieves enriched company data from Agent.ai by domain. |

### Company Earnings

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Earnings Info](actions/get-company-earnings-info.md) | GET | Retrieves company earnings information from Agent.ai by stock symbol. |

### Company Financial Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Financial Profile](actions/get-company-financial-profile.md) | GET | Retrieves company financial profiles from Agent.ai by stock symbol. |

### Domain Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Information](actions/get-domain-information.md) | GET | Retrieves domain registration data from Agent.ai by domain. |

### Google News Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Google News Data](actions/get-google-news-data.md) | GET | Finds Google News articles in Agent.ai by query. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | POST | Creates an AI-generated image in Agent.ai. |

### Instagram Follower

| Action | Method | Description |
| --- | --- | --- |
| [Get Instagram Followers](actions/get-instagram-followers.md) | GET | Retrieves Instagram followers from Agent.ai by username. |

### Instagram Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Instagram Profile](actions/get-instagram-profile.md) | GET | Retrieves an Instagram profile from Agent.ai by username. |

### Linkedin Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get LinkedIn Activity](actions/get-linkedin-activity.md) | GET | Retrieves LinkedIn posts from Agent.ai by profile URL. |

### Linkedin Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get LinkedIn Profile](actions/get-linkedin-profile.md) | GET | Retrieves a LinkedIn profile from Agent.ai by handle. |

### Linkedin Profile Slug

| Action | Method | Description |
| --- | --- | --- |
| [Find LinkedIn Profile](actions/find-linkedin-profile.md) | GET | Finds a LinkedIn profile slug in Agent.ai. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Results](actions/get-search-results.md) | GET | Finds Google or YouTube results in Agent.ai by query. |

### Tweet

| Action | Method | Description |
| --- | --- | --- |
| [Get Recent Tweets](actions/get-recent-tweets.md) | GET | Retrieves recent tweets from Agent.ai by Twitter handle. |

### Twitter User

| Action | Method | Description |
| --- | --- | --- |
| [Get Twitter Users](actions/get-twitter-users.md) | GET | Finds Twitter user profiles in Agent.ai by keywords. |

### Web Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Web Page Content](actions/get-web-page-content.md) | GET | Retrieves web page text from Agent.ai by URL or domain. |

### Web Page Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Capture Web Page Screenshot](actions/capture-web-page-screenshot.md) | GET | Captures a web page screenshot in Agent.ai by URL. |

### Youtube Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Channel Data](actions/get-youtube-channel-data.md) | GET | Retrieves YouTube channel data from Agent.ai by channel or video URL. |

### Youtube Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Search Results](actions/get-youtube-search-results.md) | GET | Finds YouTube search results in Agent.ai by query. |

### Youtube Video Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Video Transcript](actions/get-youtube-video-transcript.md) | GET | Retrieves a YouTube transcript from Agent.ai by video URL. |

