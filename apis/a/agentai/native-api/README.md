# Agent.ai: Native API Reference

A consolidated summary of Agent.ai's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.agent.ai/api-reference
- **API base URL:** `https://api-lr.agent.ai/v1`

## Authentication

### API Key

Use your Agent.ai API token as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.agent.ai/api-reference/get-data/web-page-content)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture Web Page Screenshot](actions/capture-web-page-screenshot.md) | `POST /action/grab_web_screenshot` | [docs](https://docs.agent.ai/api-reference/get-data/web-page-screenshot) |
| [Convert Text To Speech](actions/convert-text-to-speech.md) | `POST /action/output_audio` | [docs](https://docs.agent.ai/api-reference/use-ai/convert-text-to-speech) |
| [Enrich Company Data](actions/enrich-company-data.md) | `POST /action/get_company_object` | [docs](https://docs.agent.ai/api-reference/get-data/enrich-company-data) |
| [Find LinkedIn Profile](actions/find-linkedin-profile.md) | `POST /action/find_linkedin_profile` | [docs](https://docs.agent.ai/api-reference/get-data/find-linkedin-profile) |
| [Generate Image](actions/generate-image.md) | `POST /action/generate_image` | [docs](https://docs.agent.ai/api-reference/use-ai/generate-image) |
| [Get Bluesky Posts](actions/get-bluesky-posts.md) | `POST /action/get_bluesky_posts` | [docs](https://docs.agent.ai/api-reference/get-data/get-bluesky-posts) |
| [Get Company Earnings Info](actions/get-company-earnings-info.md) | `POST /action/company_financial_info` | [docs](https://docs.agent.ai/api-reference/get-data/get-company-earnings-info) |
| [Get Company Financial Profile](actions/get-company-financial-profile.md) | `POST /action/company_financial_profile` | [docs](https://docs.agent.ai/api-reference/get-data/get-company-financial-profile) |
| [Get Domain Information](actions/get-domain-information.md) | `POST /action/domain_info` | [docs](https://docs.agent.ai/api-reference/get-data/get-domain-information) |
| [Get Google News Data](actions/get-google-news-data.md) | `POST /action/get_google_news` | [docs](https://docs.agent.ai/api-reference/get-data/google-news-data) |
| [Get Instagram Followers](actions/get-instagram-followers.md) | `POST /action/get_instagram_followers` | [docs](https://docs.agent.ai/api-reference/get-data/get-instagram-followers) |
| [Get Instagram Profile](actions/get-instagram-profile.md) | `POST /action/get_instagram_profile` | [docs](https://docs.agent.ai/api-reference/get-data/get-instagram-profile) |
| [Get LinkedIn Activity](actions/get-linkedin-activity.md) | `POST /action/get_linkedin_activity` | [docs](https://docs.agent.ai/api-reference/get-data/get-linkedin-activity) |
| [Get LinkedIn Profile](actions/get-linkedin-profile.md) | `POST /action/get_linkedin_profile` | [docs](https://docs.agent.ai/api-reference/get-data/get-linkedin-profile) |
| [Get Recent Tweets](actions/get-recent-tweets.md) | `POST /action/get_recent_tweets` | [docs](https://docs.agent.ai/api-reference/get-data/get-recent-tweets) |
| [Get Search Results](actions/get-search-results.md) | `POST /action/get_search_results` | [docs](https://docs.agent.ai/api-reference/get-data/search-results) |
| [Get Twitter Users](actions/get-twitter-users.md) | `POST /action/get_twitter_users` | [docs](https://docs.agent.ai/api-reference/get-data/get-twitter-users) |
| [Get Web Page Content](actions/get-web-page-content.md) | `POST /action/grab_web_text` | [docs](https://docs.agent.ai/api-reference/get-data/web-page-content) |
| [Get YouTube Channel Data](actions/get-youtube-channel-data.md) | `POST /action/get_youtube_channel` | [docs](https://docs.agent.ai/api-reference/get-data/youtube-channel-data) |
| [Get YouTube Search Results](actions/get-youtube-search-results.md) | `POST /action/run_youtube_search` | [docs](https://docs.agent.ai/api-reference/get-data/youtube-search-results) |
| [Get YouTube Video Transcript](actions/get-youtube-video-transcript.md) | `POST /action/get_youtube_transcript` | [docs](https://docs.agent.ai/api-reference/get-data/youtube-video-transcript) |
| [Invoke Agent](actions/invoke-agent.md) | `POST /action/invoke_agent` | [docs](https://docs.agent.ai/api-reference/advanced/invoke-agent) |
| [Search Bluesky Posts](actions/search-bluesky-posts.md) | `POST /action/search_bluesky_posts` | [docs](https://docs.agent.ai/api-reference/get-data/search-bluesky-posts) |
| [Use GenAI](actions/use-genai.md) | `POST /action/invoke_llm` | [docs](https://docs.agent.ai/api-reference/use-ai/use-genai-llm) |
