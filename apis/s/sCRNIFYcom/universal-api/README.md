# <img src="https://images.mindcloud.co/apps/icons/scrnify-logo-black-2048_1776102420080.png" alt="SCRNIFY.com logo" width="28" height="28"> SCRNIFY.com: Universal API

Capture screenshots and videos from web pages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sCRNIFYcom/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scrnify.com
- **Vendor API docs:** https://scrnify.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Capture Screenshot or Video](actions/capture-screenshot-or-video.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-screenshot-or-video?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&format=0&type=0&width=1280" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Capture Cached JPEG Screenshot](actions/capture-cached-jpeg-screenshot.md) | GET | Captures or reuses a cached JPEG screenshot with SCRNIFY.com. |
| [Capture Cached MP4 Video](actions/capture-cached-mp4-video.md) | GET | Captures or reuses a cached MP4 video with SCRNIFY.com. |
| [Capture Cached PNG Screenshot](actions/capture-cached-png-screenshot.md) | GET | Captures or reuses a cached PNG screenshot with SCRNIFY.com. |
| [Capture Desktop MP4 Video](actions/capture-desktop-mp4-video.md) | GET | Captures a desktop MP4 video with SCRNIFY.com. |
| [Capture Desktop PNG Screenshot](actions/capture-desktop-png-screenshot.md) | GET | Captures a desktop PNG screenshot with SCRNIFY.com. |
| [Capture Full Page JPEG Screenshot](actions/capture-full-page-jpeg-screenshot.md) | GET | Captures a full-page JPEG screenshot with SCRNIFY.com. |
| [Capture Full Page PNG Screenshot](actions/capture-full-page-png-screenshot.md) | GET | Captures a full-page PNG screenshot with SCRNIFY.com. |
| [Capture GIF Screenshot](actions/capture-gif-screenshot.md) | GET | Captures a GIF screenshot with SCRNIFY.com. |
| [Capture GIF Video](actions/capture-gif-video.md) | GET | Captures a GIF video with SCRNIFY.com. |
| [Capture JPEG Screenshot](actions/capture-jpeg-screenshot.md) | GET | Captures a JPEG screenshot with SCRNIFY.com. |
| [Capture Mobile MP4 Video](actions/capture-mobile-mp4-video.md) | GET | Captures a mobile MP4 video with SCRNIFY.com. |
| [Capture Mobile PNG Screenshot](actions/capture-mobile-png-screenshot.md) | GET | Captures a mobile PNG screenshot with SCRNIFY.com. |
| [Capture MP4 Video](actions/capture-mp4-video.md) | GET | Captures an MP4 video with SCRNIFY.com. |
| [Capture MP4 Video After Load](actions/capture-mp4-video-after-load.md) | GET | Captures an MP4 video with SCRNIFY.com after the load event. |
| [Capture PNG Screenshot](actions/capture-png-screenshot.md) | GET | Captures a PNG screenshot with SCRNIFY.com. |
| [Capture Screenshot After DOMContentLoaded](actions/capture-screenshot-after-dom-content-loaded.md) | GET | Captures a screenshot with SCRNIFY.com after DOMContentLoaded. |
| [Capture Screenshot After First Contentful Paint](actions/capture-screenshot-after-first-contentful-paint.md) | GET | Captures a screenshot with SCRNIFY.com after first contentful paint. |
| [Capture Screenshot After First Meaningful Paint](actions/capture-screenshot-after-first-meaningful-paint.md) | GET | Captures a screenshot with SCRNIFY.com after first meaningful paint. |
| [Capture Screenshot After Load](actions/capture-screenshot-after-load.md) | GET | Captures a screenshot with SCRNIFY.com after the load event. |
| [Capture Screenshot After Network Idle](actions/capture-screenshot-after-network-idle.md) | GET | Captures a screenshot with SCRNIFY.com after network idle. |
| [Capture Screenshot or Video](actions/capture-screenshot-or-video.md) | GET | Captures a screenshot or video with SCRNIFY.com. |
| [Capture Screenshot with Cookies Allowed](actions/capture-screenshot-with-cookies-allowed.md) | GET | Captures a screenshot with cookies allowed in SCRNIFY.com. |
| [Capture Screenshot with Custom User Agent](actions/capture-screenshot-with-custom-user-agent.md) | GET | Captures a screenshot in SCRNIFY.com with a custom user agent. |
| [Capture Selector JPEG Screenshot](actions/capture-selector-jpeg-screenshot.md) | GET | Captures a JPEG screenshot of a selected element with SCRNIFY.com. |
| [Capture Selector MP4 Video](actions/capture-selector-mp4-video.md) | GET | Captures an MP4 video of a selected element with SCRNIFY.com. |
| [Capture Selector PNG Screenshot](actions/capture-selector-png-screenshot.md) | GET | Captures a PNG screenshot of a selected element with SCRNIFY.com. |
| [Capture Short GIF Video](actions/capture-short-gif-video.md) | GET | Captures a short GIF video with SCRNIFY.com. |
| [Capture Short MP4 Video](actions/capture-short-mp4-video.md) | GET | Captures a short MP4 video with SCRNIFY.com. |
| [Capture WEBM Video](actions/capture-webm-video.md) | GET | Captures a WEBM video with SCRNIFY.com. |
| [Capture WEBM Video After Network Idle](actions/capture-webm-video-after-network-idle.md) | GET | Captures a WEBM video with SCRNIFY.com after network idle. |

