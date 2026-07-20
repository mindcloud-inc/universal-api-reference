# QuestionScout: Native API Reference

A consolidated summary of QuestionScout's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://support.questionscout.com/category/31-sharing-embedding
- **API base URL:** `https://api2.questionscout.com/wordpress`

## Authentication

### API Key (Query)

Use the QuestionScout account API key in the shared `key` query parameter.

### Credentials

- **API Key:** `apiKey` · required · QuestionScout account API key from the Integrations page. MindCloud sends it as the shared `key` query parameter.

[Official authentication documentation](https://wordpress.org/plugins/questionscout/)

## API conventions

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://support.questionscout.com/article/18-questionscout-wordpress) |
