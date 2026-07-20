# SMSMagic: Native API Reference

A consolidated summary of SMSMagic's API configuration, with links to official documentation.

- **Official docs:** https://api.sms-magic.com/doc/
- **API base URL:** `https://api.sms-magic.com`

## Authentication

### API Key

Authenticate with the SMSMagic API key issued for the SMSMagic account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apiKey: <apiKey>
```

[Official authentication documentation](https://api.sms-magic.com/doc/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.
