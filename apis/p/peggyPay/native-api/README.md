# Peggy Pay: Native API Reference

A consolidated summary of Peggy Pay's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.peggypay.com/kennisbank
- **API base URL:** `https://www.peggypay.com/api`

## Authentication

### API Key Token Exchange

Connect Peggy Pay with an API key, then exchange it for a Peggy Pay session token.

### Credentials

- **API Key:** `apiKey` · required · Peggy Pay API key from the Peggy account API keys page.

[Official authentication documentation](https://github.com/peggyforms/php-sdk)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Submission Item](actions/add-submission-item.md) | `GET Formbuilder.Submissions.addItem` | [docs](https://github.com/peggyforms/php-sdk/blob/master/src/Modules/Submissions.php) |
| [Authorize API Key](actions/authorize-api-key.md) | `GET Framework.authorize` | [docs](https://github.com/peggyforms/php-sdk/blob/master/src/Api.php) |
| [Get Order by Order Hash](actions/get-order-by-order-hash.md) | `GET Formbuilder.Submissions.getOrder` | [docs](https://github.com/peggyforms/php-sdk/blob/master/src/Modules/Orders.php) |
| [Get Order by Submission Hash](actions/get-order-by-submission-hash.md) | `GET Formbuilder.Submissions.getOrder` | [docs](https://github.com/peggyforms/php-sdk/blob/master/src/Modules/Orders.php) |
| [Get Submission by Hash](actions/get-submission-by-hash.md) | `GET Formbuilder.Submissions.getSubmissionByHash` | [docs](https://github.com/peggyforms/php-sdk/blob/master/src/Modules/Submissions.php) |
