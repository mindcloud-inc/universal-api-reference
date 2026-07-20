# ChurchStamp: Native API Reference

A consolidated summary of ChurchStamp's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://churchstampapi.docs.apiary.io/
- **OpenAPI specification:** https://churchstampapi.docs.apiary.io/api-description-document
- **API base URL:** `https://v2.churchstamp.com/api/1.1/wf`

## Authentication

### Access Token

ChurchStamp access token used as the shared access_token query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://churchstampapi.docs.apiary.io/introduction/authentication)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete a Design](actions/delete-a-design.md) | `POST /delete-design` | [docs](https://churchstampapi.docs.apiary.io/reference/designs/delete-a-design) |
| [Get a Campaign](actions/get-a-campaign.md) | `GET /get-a-campaigns` | [docs](https://churchstampapi.docs.apiary.io/reference/campaigns/get-a-campaign) |
| [Get a Design](actions/get-a-design.md) | `GET /get-a-design` | [docs](https://churchstampapi.docs.apiary.io/reference/designs/get-a-design) |
| [Get Campaigns](actions/get-campaigns.md) | `GET /get-campaigns` | [docs](https://churchstampapi.docs.apiary.io/reference/campaigns/get-campaigns) |
| [Get Designs](actions/get-designs.md) | `GET /get-designs` | [docs](https://churchstampapi.docs.apiary.io/reference/designs/get-designs) |
| [Get User Details](actions/get-user-details.md) | `GET /get-user` | [docs](https://churchstampapi.docs.apiary.io/reference/account/get-user-details) |
| [Send Mail](actions/send-mail.md) | `POST /campaign-sendmail` | [docs](https://churchstampapi.docs.apiary.io/reference/campaigns/send-mail) |
