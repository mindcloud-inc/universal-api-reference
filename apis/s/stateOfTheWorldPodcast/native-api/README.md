# State of the World Podcast: Native API Reference

A consolidated summary of State of the World Podcast's API configuration, with links to official documentation.

- **Official docs:** https://feeds.npr.org/510366/podcast.xml
- **API base URL:** `https://feeds.npr.org`

## Authentication

### No authentication

Public NPR podcast RSS feed; no credentials are required.

This API does not require request authentication.

[Official authentication documentation](https://feeds.npr.org/510366/podcast.xml)

## API conventions

Responses from this API use XML. Response data is read from `rss.channel.item`.
