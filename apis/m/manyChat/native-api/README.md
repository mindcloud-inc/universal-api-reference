# ManyChat: Native API Reference

A consolidated summary of ManyChat's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://api.manychat.com/swagger
- **OpenAPI specification:** https://api.manychat.com/swagger/compileJson?type=Page_API
- **API base URL:** `https://api.manychat.com`

## Authentication

### API Key

Authenticate with a ManyChat Public API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.manychat.com/hc/en-us/articles/14959510331420-How-to-generate-a-token-for-the-Manychat-API-and-where-to-get-parameters)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tag To Subscriber](actions/add-tag-to-subscriber.md) | `POST /fb/subscriber/addTag` | [docs](https://api.manychat.com/swagger#/Subscriber/ee797ad59ec8545bed43add11390b165) |
| [Add Tag To Subscriber By Name](actions/add-tag-to-subscriber-by-name.md) | `POST /fb/subscriber/addTagByName` | [docs](https://api.manychat.com/swagger#/Subscriber/34ad004a12043ccbfee2faf1d290d30f) |
| [Create Bot Field](actions/create-bot-field.md) | `POST /fb/page/createBotField` | [docs](https://api.manychat.com/swagger#/Page/388714b65c83021aa8b1bb78481fb983) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /fb/page/createCustomField` | [docs](https://api.manychat.com/swagger#/Page/1d7171252e09f4e25b5123f9484ea3c1) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /fb/subscriber/createSubscriber` | [docs](https://api.manychat.com/swagger#/Subscriber/f42eb3580f33178fdf9d87f0c778f86e) |
| [Create Tag](actions/create-tag.md) | `POST /fb/page/createTag` | [docs](https://api.manychat.com/swagger#/Page/e964547412ede512f9534970c8e3971a) |
| [Get Page Info](actions/get-page-info.md) | `GET /fb/page/getInfo` | [docs](https://api.manychat.com/swagger#/Page/b26c074b3783eb6e888c62324b17268c) |
| [Get Subscriber Info](actions/get-subscriber-info.md) | `GET /fb/subscriber/getInfo` | [docs](https://api.manychat.com/swagger#/Subscriber/ae51a27b65b7ecf39438af38db0f27ba) |
| [Get Subscriber Info By User Ref](actions/get-subscriber-info-by-user-ref.md) | `GET /fb/subscriber/getInfoByUserRef` | [docs](https://api.manychat.com/swagger#/Subscriber/782cc8abe7878dc73026b6bef44f14b2) |
| [List Bot Fields](actions/list-bot-fields.md) | `GET /fb/page/getBotFields` | [docs](https://api.manychat.com/swagger#/Page/dbb46d786cc1323d56b27ff7de7bcc3f) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /fb/page/getCustomFields` | [docs](https://api.manychat.com/swagger#/Page/2bc43834222da265c4c41fbd129d1392) |
| [List Flows](actions/list-flows.md) | `GET /fb/page/getFlows` | [docs](https://api.manychat.com/swagger#/Page/6aee779784709b84bb0a734ebb42b650) |
| [List Growth Tools](actions/list-growth-tools.md) | `GET /fb/page/getGrowthTools` | [docs](https://api.manychat.com/swagger#/Page/2ab4a2a91a0b2cb1d5084e91b281e48c) |
| [List Tags](actions/list-tags.md) | `GET /fb/page/getTags` | [docs](https://api.manychat.com/swagger#/Page/55f8b0c6040a20ba811a08eb4d92b9c2) |
| [Remove Tag](actions/remove-tag.md) | `POST /fb/page/removeTag` | [docs](https://api.manychat.com/swagger#/Page/55b1d844eb0006f3c49e2a3ac524dd4e) |
| [Remove Tag From Subscriber](actions/remove-tag-from-subscriber.md) | `POST /fb/subscriber/removeTag` | [docs](https://api.manychat.com/swagger#/Subscriber/09f35f7c1e6013311f36e3965dec650c) |
| [Remove Tag From Subscriber By Name](actions/remove-tag-from-subscriber-by-name.md) | `POST /fb/subscriber/removeTagByName` | [docs](https://api.manychat.com/swagger#/Subscriber/59cef9685d8978968b28376db0123be4) |
| [Search Subscribers by Custom Field](actions/search-subscribers-by-custom-field.md) | `GET /fb/subscriber/findByCustomField` | [docs](https://api.manychat.com/swagger#/Subscriber/9fc380dcb49bb134b9405d4269896f56) |
| [Search Subscribers by Name](actions/search-subscribers-by-name.md) | `GET /fb/subscriber/findByName` | [docs](https://api.manychat.com/swagger#/Subscriber/e5c671d1661acff9be0e8bcfdd59f1e8) |
| [Search Subscribers by System Field](actions/search-subscribers-by-system-field.md) | `GET /fb/subscriber/findBySystemField` | [docs](https://api.manychat.com/swagger#/Subscriber/ef59064a933ef7464083a39c520a274b) |
| [Send Content](actions/send-content.md) | `POST /fb/sending/sendContent` | [docs](https://api.manychat.com/swagger#/Sending/b6ae94031676b69a57eb2ad5ea1413f9) |
| [Send Flow](actions/send-flow.md) | `POST /fb/sending/sendFlow` | [docs](https://api.manychat.com/swagger#/Sending/28f1abbb07b0d4773b846dbeb3880e3c) |
| [Set Bot Field](actions/set-bot-field.md) | `POST /fb/page/setBotField` | [docs](https://api.manychat.com/swagger#/Page/4032722e43e4b967e07d1b1279942254) |
| [Set Bot Fields](actions/set-bot-fields.md) | `POST /fb/page/setBotFields` | [docs](https://api.manychat.com/swagger#/Page/327327a53f87fecaeb9f7cd69c0433af) |
| [Set Subscriber Custom Field](actions/set-subscriber-custom-field.md) | `POST /fb/subscriber/setCustomField` | [docs](https://api.manychat.com/swagger#/Subscriber/81138a426b0903687848fdf8bdde6aa9) |
| [Set Subscriber Custom Field By Name](actions/set-subscriber-custom-field-by-name.md) | `POST /fb/subscriber/setCustomFieldByName` | [docs](https://api.manychat.com/swagger#/Subscriber/adc69e1e87197b5f31c80403a3913468) |
| [Set Subscriber Custom Fields](actions/set-subscriber-custom-fields.md) | `POST /fb/subscriber/setCustomFields` | [docs](https://api.manychat.com/swagger#/Subscriber/4d01076149250e9e47f3b8aa7dc53baa) |
| [Update Subscriber](actions/update-subscriber.md) | `POST /fb/subscriber/updateSubscriber` | [docs](https://api.manychat.com/swagger#/Subscriber/3ab84a004f4a5942e7a5368c2b807d19) |
