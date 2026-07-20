# King County Metro: Native API Reference

A consolidated summary of King County Metro's API configuration, with links to official documentation.

- **Official docs:** https://kingcounty.gov/en/dept/metro/rider-tools/mobile-and-web-apps#toc-developer-resources
- **API base URL:** `https://s3.amazonaws.com/kcm-alerts-realtime-prod`

## Authentication

### No Authentication

King County Metro's public GTFS and GTFS-Realtime feeds are available without provider-side authentication for the selected public feed path.

This API does not require request authentication.

[Official authentication documentation](https://kingcounty.gov/en/dept/metro/rider-tools/mobile-and-web-apps#toc-developer-resources)

## API conventions

Responses from this API use JSON. Response data is read from `entity`.
