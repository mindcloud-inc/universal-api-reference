# Did You Mean This: Native API Reference

A consolidated summary of Did You Mean This's API configuration, with links to official documentation.

- **Official docs:** https://marketplace.apilayer.com/dymt-api/tabs/api_docs
- **API base URL:** `https://api.apilayer.com/dymt`

## Authentication

### API Key

APILayer API key sent in the required apikey HTTP header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://marketplace.apilayer.com/dymt-api/tabs/api_docs)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.
