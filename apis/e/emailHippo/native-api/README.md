# Email Hippo: Native API Reference

A consolidated summary of Email Hippo's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.emailhippo.com/
- **API base URL:** `https://api.hippoapi.com`

## Authentication

### API Key

Email Hippo license key injected into provider-specific query and path parameters.

[Official authentication documentation](https://docs.emailhippo.com/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Quota Usage](actions/get-quota-usage.md) | `GET customer/reports/v3/quota/{{credentials.apiKey}}` | [docs](https://docs.emailhippo.com/) |
| [Verify Email (MORE V2)](actions/verify-email-morev2.md) | `GET https://api1.27hub.com/api/emh/a/v2?k={{credentials.apiKey}}&e=:emailAddress` | [docs](https://docs.emailhippo.com/) |
| [Verify Email (MORE V3 BSON)](actions/verify-email-morev3-bson.md) | `GET v3/more/bson/{{credentials.apiKey}}/:emailAddress` | [docs](https://docs.emailhippo.com/) |
| [Verify Email (MORE V3 JSON)](actions/verify-email-morev3-json.md) | `GET v3/more/json/{{credentials.apiKey}}/:emailAddress` | [docs](https://docs.emailhippo.com/) |
| [Verify Email (MORE V3 Protobuf)](actions/verify-email-morev3-protobuf.md) | `GET v3/more/proto/{{credentials.apiKey}}/:emailAddress` | [docs](https://docs.emailhippo.com/) |
| [Verify Email (MORE V3 XML)](actions/verify-email-morev3-xml.md) | `GET v3/more/xml/{{credentials.apiKey}}/:emailAddress` | [docs](https://docs.emailhippo.com/) |
