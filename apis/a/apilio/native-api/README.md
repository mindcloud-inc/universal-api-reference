# Apilio: Native API Reference

A consolidated summary of Apilio's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/13480928/TzCHAVD2
- **API base URL:** `https://api.apilio.com`

## Authentication

### Basic Auth

Authenticate Apilio REST API requests with the API username and API password from the Apilio profile page.

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

[Official authentication documentation](https://documenter.getpostman.com/view/13480928/TzCHAVD2)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Evaluate Logicblock](actions/evaluate-logicblock.md) | `POST /api/v1/logicblocks/{{uuid}}/evaluate` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Get Boolean Variable](actions/get-boolean-variable.md) | `GET /api/v1/boolean_variables/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Get Numeric Variable](actions/get-numeric-variable.md) | `GET /api/v1/numeric_variables/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Get String Variable](actions/get-string-variable.md) | `GET /api/v1/string_variables/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Get Time Condition](actions/get-time-condition.md) | `GET /api/v1/timeconditions/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Get Tuya Condition](actions/get-tuya-condition.md) | `GET /api/v1/tuyaconditions/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Get Variable Condition](actions/get-variable-condition.md) | `GET /api/v1/variableconditions/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [List Boolean Variables](actions/list-boolean-variables.md) | `GET /api/v1/boolean_variables` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [List Conditions](actions/list-conditions.md) | `GET /api/v1/conditions` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [List Logicblocks](actions/list-logicblocks.md) | `GET /api/v1/logicblocks` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [List Numeric Variables](actions/list-numeric-variables.md) | `GET /api/v1/numeric_variables` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [List String Variables](actions/list-string-variables.md) | `GET /api/v1/string_variables` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [List Time Conditions](actions/list-time-conditions.md) | `GET /api/v1/timeconditions` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [List Tuya Conditions](actions/list-tuya-conditions.md) | `GET /api/v1/tuyaconditions` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [List Variable Conditions](actions/list-variable-conditions.md) | `GET /api/v1/variableconditions` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Set Logicblock Active State](actions/set-logicblock-active-state.md) | `PATCH /api/v1/logicblocks/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Update Boolean Variable](actions/update-boolean-variable.md) | `PUT /api/v1/boolean_variables/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Update Numeric Variable](actions/update-numeric-variable.md) | `PUT /api/v1/numeric_variables/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
| [Update String Variable](actions/update-string-variable.md) | `PUT /api/v1/string_variables/{{uuid}}` | [docs](https://documenter.getpostman.com/view/13480928/TzCHAVD2) |
