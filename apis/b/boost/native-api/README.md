# Boost: Native API Reference

A consolidated summary of Boost's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://apidoc.boost.space/
- **OpenAPI specification:** https://apidoc.boost.space/latest.json
- **API base URL:** `https://{systemKey}.boost.space/api`

## Authentication

### API token

Authenticate with a Boost.space API token. The system key is the workspace subdomain from the Boost.space URL.

### Credentials

- **API Key:** `apiKey` · required
- **System key:** `systemKey` · required · The Boost.space workspace subdomain before .boost.space, for example test-system from test-system.boost.space.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.boost.space/knowledge-base/integrations/bse-connections/how-to-create-a-boost-space-connection-system-key-api-token/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`, `neq`.

## Sorting

Set the sort field with `order` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | `GET /activities/{activityId}` | [docs](https://apidoc.boost.space/) |
| [Get Address](actions/get-address.md) | `GET /address/{addressId}` | [docs](https://apidoc.boost.space/) |
| [Get AppFlow](actions/get-appflow.md) | `GET /appflow/{appflowId}` | [docs](https://apidoc.boost.space/) |
| [Get Automation Action](actions/get-automation-action.md) | `GET /automatization/action/{actionId}` | [docs](https://apidoc.boost.space/) |
| [Get Automation Trigger](actions/get-automation-trigger.md) | `GET /automatization/trigger/{triggerId}` | [docs](https://apidoc.boost.space/) |
| [Get Business Case](actions/get-business-case.md) | `GET /business-case/{businessCaseId}` | [docs](https://apidoc.boost.space/) |
| [Get Contact](actions/get-contact.md) | `GET /contact/{contactId}` | [docs](https://apidoc.boost.space/) |
| [Get Custom Module](actions/get-custom-module.md) | `GET /custom-module/{customModuleId}` | [docs](https://apidoc.boost.space/) |
| [Get File](actions/get-file.md) | `GET /file/{fileId}` | [docs](https://apidoc.boost.space/) |
| [Get Form](actions/get-form.md) | `GET /form/{formId}` | [docs](https://apidoc.boost.space/) |
| [Get Space](actions/get-space.md) | `GET /space/{spaceId}` | [docs](https://apidoc.boost.space/) |
| [Get User](actions/get-user.md) | `GET /user/{userId}` | [docs](https://apidoc.boost.space/) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://apidoc.boost.space/) |
| [List Addresses](actions/list-addresses.md) | `GET /address` | [docs](https://apidoc.boost.space/) |
| [List AppFlows](actions/list-appflows.md) | `GET /appflow` | [docs](https://apidoc.boost.space/) |
| [List Automation Actions](actions/list-automation-actions.md) | `GET /automatization/action` | [docs](https://apidoc.boost.space/) |
| [List Automation Triggers](actions/list-automation-triggers.md) | `GET /automatization/trigger` | [docs](https://apidoc.boost.space/) |
| [List Business Cases](actions/list-business-cases.md) | `GET /business-case` | [docs](https://apidoc.boost.space/) |
| [List Business Contracts](actions/list-business-contracts.md) | `GET /business-contract` | [docs](https://apidoc.boost.space/) |
| [List Business Offers](actions/list-business-offers.md) | `GET /business-offer` | [docs](https://apidoc.boost.space/) |
| [List Business Orders](actions/list-business-orders.md) | `GET /business-order` | [docs](https://apidoc.boost.space/) |
| [List Charts](actions/list-charts.md) | `GET /chart` | [docs](https://apidoc.boost.space/) |
| [List Contacts](actions/list-contacts.md) | `GET /contact` | [docs](https://apidoc.boost.space/) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-field` | [docs](https://apidoc.boost.space/) |
| [List Custom Modules](actions/list-custom-modules.md) | `GET /custom-module` | [docs](https://apidoc.boost.space/) |
| [List Dashboards](actions/list-dashboards.md) | `GET /dashboard` | [docs](https://apidoc.boost.space/) |
| [List Files](actions/list-files.md) | `GET /file/` | [docs](https://apidoc.boost.space/) |
| [List Forms](actions/list-forms.md) | `GET /form` | [docs](https://apidoc.boost.space/) |
| [List Spaces](actions/list-spaces.md) | `GET /space` | [docs](https://apidoc.boost.space/) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://apidoc.boost.space/) |
