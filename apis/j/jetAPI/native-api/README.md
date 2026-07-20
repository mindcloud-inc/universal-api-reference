# JetAPI: Native API Reference

A consolidated summary of JetAPI's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.jetapi.io/
- **API base URL:** `https://api.jetapi.io`

## Authentication

### Bearer Token

Use your JetAPI developer token as a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.jetapi.io/view/metadata/2sA2r834S1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bulk Delivery](actions/create-bulk-delivery.md) | `POST /api/v1/bulk_delivery` | [docs](https://docs.jetapi.io/#1f668b73-8439-43d2-bb7f-95942c5da96d) |
| [Create Chat Link](actions/create-chat-link.md) | `POST /api/v1/chatter/` | [docs](https://docs.jetapi.io/#df8a4c17-418b-41f8-b3ad-fbb018210e1a) |
| [Create Delivery](actions/create-delivery.md) | `POST /api/v1/delivery` | [docs](https://docs.jetapi.io/#ea49fe72-5621-405c-ba99-8450050a35ff) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v1/webhooks` | [docs](https://docs.jetapi.io/#1acdd39e-f338-4664-8aa9-07bd1b875556) |
| [Delete Chatter Session](actions/delete-chatter-session.md) | `DELETE /api/v1/chatter/` | [docs](https://docs.jetapi.io/#b3104089-5b1f-48b5-9fa4-203e63a44140) |
| [Delete Developer Chat](actions/delete-developer-chat.md) | `DELETE /api/developer_chat/` | [docs](https://docs.jetapi.io/#d3c6246f-145b-4475-96cb-f4f4d677b82e) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v1/webhooks/:id` | [docs](https://docs.jetapi.io/#4b696871-b1f5-4118-898e-d6802502fec9) |
| [Get Account](actions/get-account.md) | `GET /api/v1/account` | [docs](https://docs.jetapi.io/api/collections/31634267/2sA2r834S1?segregateAuth=true&versionTag=latest) |
| [Get Delivery Status](actions/get-delivery-status.md) | `GET /api/v1/delivery/:id` | [docs](https://docs.jetapi.io/#7b1aa4db-cbfe-4335-b0f1-17e9f3d4c490) |
| [Get UTM Tags](actions/get-utm-tags.md) | `GET /api/v1/utm_mark` | [docs](https://docs.jetapi.io/#ae5be06e-2f47-446b-9865-0c90a07c09bc) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/v1/webhooks/:id` | [docs](https://docs.jetapi.io/#97ff61cd-dbae-4da5-8e5b-b2c46e4aaf70) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v1/webhooks/` | [docs](https://docs.jetapi.io/#0c39852e-584d-4300-8621-a1a9b486ffa2) |
| [Lookup Phone Operator](actions/lookup-phone-operator.md) | `GET /api/v1/operators/search` | [docs](https://docs.jetapi.io/#c22bc81c-94fe-4a10-b48e-6b6d5ef3089b) |
| [Open Developer Chat By Phone](actions/open-developer-chat-by-phone.md) | `GET /developer_chat` | [docs](https://docs.jetapi.io/#ca99f0ce-984e-40ee-ba7a-8678c240bea6) |
| [Open Dialog By Phone](actions/open-dialog-by-phone.md) | `GET /api/v1/chatter/` | [docs](https://docs.jetapi.io/#eef20d97-d724-43b3-b08a-7f0f04884762) |
| [Send File](actions/send-file.md) | `POST /api/v1/send_file` | [docs](https://docs.jetapi.io/#2527e2f5-c9be-4925-8657-a76116267816) |
| [Update Chat Notes](actions/update-chat-notes.md) | `PUT /api/developer_chat/conversations/notes` | [docs](https://docs.jetapi.io/#fde64a3c-12e8-4953-b4ef-363078153aaa) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /api/v1/webhooks/:id` | [docs](https://docs.jetapi.io/#96d9833d-7367-4b14-9d8c-a152360e608a) |
