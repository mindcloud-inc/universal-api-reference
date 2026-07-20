# Cyfe: Native API Reference

A consolidated summary of Cyfe's API configuration, with links to official documentation.

- **Official docs:** https://www.cyfe.com/api/
- **API base URL:** `https://app.cyfe.com/api/push`

## Authentication

### Push API Widget Endpoint

Connect one Cyfe Push API widget by saving its widget endpoint key.

### Credentials

- **Widget Endpoint Key:** `widgetEndpointKey` · required · The final path segment from the Cyfe Push API widget API Endpoint URL.

[Official authentication documentation](https://www.cyfe.com/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
