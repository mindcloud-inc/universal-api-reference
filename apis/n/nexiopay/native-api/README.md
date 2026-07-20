# Nexiopay: Native API Reference

A consolidated summary of Nexiopay's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.nexiopay.com/reference
- **API base URL:** `https://api.nexiopaysandbox.com`

## Authentication

### Basic authentication

Authenticate with a Nexio API username and API key used as the Basic-auth password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.nexiopay.com/docs/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture a transaction](actions/capture-a-transaction.md) | `POST /pay/v3/capture` | [docs](https://docs.nexiopay.com/reference/capturetransaction) |
| [Capture an APM transaction](actions/capture-an-apm-transaction.md) | `POST /apm/v3/capture` | [docs](https://docs.nexiopay.com/reference/captureapmtransaction) |
| [Create APM one-time-use token](actions/create-apm-one-time-use-token.md) | `POST /apm/v3/token` | [docs](https://docs.nexiopay.com/reference/createapmonetimeusetoken) |
| [Create one-time-use token](actions/create-one-time-use-token.md) | `POST /pay/v3/token` | [docs](https://docs.nexiopay.com/reference/createonetimeusetoken-1) |
| [Create simple login](actions/create-simple-login.md) | `POST /auth/v3/createSimpleLogin` | [docs](https://docs.nexiopay.com/reference/createsimplelogin) |
| [Delete card tokens](actions/delete-card-tokens.md) | `POST /pay/v3/deleteToken` | [docs](https://docs.nexiopay.com/reference/deletecardtokens) |
| [Deregister terminal](actions/deregister-terminal.md) | `POST /pay/v3/deregisterTerminal` | [docs](https://docs.nexiopay.com/reference/deregisterterminal) |
| [Get APM iframe](actions/get-apm-iframe.md) | `GET /apm/v3` | [docs](https://docs.nexiopay.com/reference/getapmiframe) |
| [Pair terminal](actions/pair-terminal.md) | `POST /pay/v3/pairTerminal` | [docs](https://docs.nexiopay.com/reference/pairterminal) |
| [Process transaction from terminal](actions/process-transaction-from-terminal.md) | `POST /pay/v3/processFromTerminal` | [docs](https://docs.nexiopay.com/reference/processtransactionfromterminal) |
| [Refund a transaction](actions/refund-a-transaction.md) | `POST /pay/v3/refund` | [docs](https://docs.nexiopay.com/reference/refundtransaction) |
| [Refund an APM transaction](actions/refund-an-apm-transaction.md) | `POST /apm/v3/refund` | [docs](https://docs.nexiopay.com/reference/refundapmtransaction) |
| [Register terminal](actions/register-terminal.md) | `POST /pay/v3/registerTerminal` | [docs](https://docs.nexiopay.com/reference/registerterminal) |
| [Run APM transaction](actions/run-apm-transaction.md) | `POST /apm/v3/process` | [docs](https://docs.nexiopay.com/reference/runapmtransaction) |
| [Run card transaction](actions/run-card-transaction.md) | `POST /pay/v3/process` | [docs](https://docs.nexiopay.com/reference/runcardtransaction) |
| [Run card transaction with iframe](actions/run-card-transaction-with-iframe.md) | `GET /pay/v3` | [docs](https://docs.nexiopay.com/reference/runcardtransactioniframe) |
| [Run echeck transaction](actions/run-echeck-transaction.md) | `POST /pay/v3/processECheck` | [docs](https://docs.nexiopay.com/reference/runechecktransaction) |
| [Run echeck transaction with iframe](actions/run-echeck-transaction-with-iframe.md) | `GET /pay/v3/processECheck` | [docs](https://docs.nexiopay.com/reference/runechecktransactioniframe) |
| [Save card token](actions/save-card-token.md) | `POST /pay/v3/saveCard` | [docs](https://docs.nexiopay.com/reference/savecardtoken) |
| [Save card token with iframe](actions/save-card-token-with-iframe.md) | `GET /pay/v3/saveCard` | [docs](https://docs.nexiopay.com/reference/savecardtokeniframe-1) |
| [Save echeck token](actions/save-echeck-token.md) | `POST /pay/v3/saveECheck` | [docs](https://docs.nexiopay.com/reference/saveechecktoken) |
| [Save echeck token with iframe](actions/save-echeck-token-with-iframe.md) | `GET /pay/v3/saveECheck` | [docs](https://docs.nexiopay.com/reference/saveechecktokeniframe) |
| [Update card token](actions/update-card-token.md) | `PUT /pay/v3/vault/card/{cardToken}` | [docs](https://docs.nexiopay.com/reference/updatecardtoken) |
| [View APM transaction async status](actions/view-apm-transaction-async-status.md) | `GET /apm/v3/transactionAsyncStatus/{asyncTraceId}` | [docs](https://docs.nexiopay.com/reference/viewapmtransactionasyncstatus) |
| [View card token details](actions/view-card-token-details.md) | `GET /pay/v3/vault/card/{cardToken}` | [docs](https://docs.nexiopay.com/reference/viewcardtokendetails) |
| [View card tokens](actions/view-card-tokens.md) | `GET /card/v3` | [docs](https://docs.nexiopay.com/reference/viewcardtokens) |
| [View currency conversion rates](actions/view-currency-conversion-rates.md) | `GET /pay/v3/conversionRates` | [docs](https://docs.nexiopay.com/reference/viewcurrencyconversionrates) |
| [View echeck token details](actions/view-echeck-token-details.md) | `GET /pay/v3/vault/echeck/{echeckToken}` | [docs](https://docs.nexiopay.com/reference/viewechecktokendetails) |
| [View merchants by ID](actions/view-merchants-by-id.md) | `GET /merchant/v3` | [docs](https://docs.nexiopay.com/reference/viewmerchantsbyid) |
| [View payouts](actions/view-payouts.md) | `GET /payout/v3` | [docs](https://docs.nexiopay.com/reference/viewpayouts) |
| [View recipients](actions/view-recipients.md) | `GET /payout/v3/recipient` | [docs](https://docs.nexiopay.com/reference/viewrecipients) |
| [View surcharge recommendation](actions/view-surcharge-recommendation.md) | `POST /pay/v3/surcharge` | [docs](https://docs.nexiopay.com/reference/viewsurchargerecommendation) |
| [View terminal list](actions/view-terminal-list.md) | `GET /pay/v3/getTerminalList` | [docs](https://docs.nexiopay.com/reference/viewterminallist) |
| [View terminal transaction status](actions/view-terminal-transaction-status.md) | `GET /pay/v3/processFromTerminal/{terminalRequestId}` | [docs](https://docs.nexiopay.com/reference/viewterminaltransactionstatus) |
| [View transaction async status](actions/view-transaction-async-status.md) | `GET /pay/v3/transactionAsyncStatus/{asyncTraceId}` | [docs](https://docs.nexiopay.com/reference/viewtransactionasyncstatus) |
| [View transaction by payment ID](actions/view-transaction-by-payment-id.md) | `GET /transaction/v3/paymentId/{paymentId}` | [docs](https://docs.nexiopay.com/reference/viewtransactionbypaymentid) |
| [View transactions](actions/view-transactions.md) | `GET /transaction/v3` | [docs](https://docs.nexiopay.com/reference/viewtransactions) |
| [Void a transaction](actions/void-a-transaction.md) | `POST /pay/v3/void` | [docs](https://docs.nexiopay.com/reference/voidtransaction) |
| [Void an APM transaction](actions/void-an-apm-transaction.md) | `POST /apm/v3/void` | [docs](https://docs.nexiopay.com/reference/voidapmtransaction) |
| [Who am I](actions/who-am-i.md) | `GET /user/v3/account/whoAmI` | [docs](https://docs.nexiopay.com/reference/whoami) |
