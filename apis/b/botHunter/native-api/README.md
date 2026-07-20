# BotHunter: Native API Reference

A consolidated summary of BotHunter's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://smm.targethunter.help/dev/api
- **API base URL:** `https://smm.targethunter.ru/api`

## Authentication

### API Key

Authenticate BotHunter API requests with the access token from BotHunter settings. The token must be supplied as the shared api_key query parameter on every API method.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://smm.targethunter.help/dev/api/api-klyuch)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User To Bot](actions/add-user-to-bot.md) | `POST /bots/addUser` | [docs](https://smm.targethunter.help/dev/api/methods/bots/adduser) |
| [Clear Community Variable](actions/clear-community-variable.md) | `POST /globalvars/clear` | [docs](https://smm.targethunter.help/dev/api/methods/globalvars/clear) |
| [Clear User Variable](actions/clear-user-variable.md) | `POST /vars/clear` | [docs](https://smm.targethunter.help/dev/api/methods/vars/clear) |
| [Get Community Variable](actions/get-community-variable.md) | `GET /globalvars/get` | [docs](https://smm.targethunter.help/dev/api/methods/globalvars/get) |
| [Get User Variable](actions/get-user-variable.md) | `GET /vars/get` | [docs](https://smm.targethunter.help/dev/api/methods/vars/get) |
| [Remove User From Bot](actions/remove-user-from-bot.md) | `POST /bots/removeUser` | [docs](https://smm.targethunter.help/dev/api/methods/bots/removeuser) |
| [Set Community Variable](actions/set-community-variable.md) | `POST /globalvars/set` | [docs](https://smm.targethunter.help/dev/api/methods/globalvars/set) |
| [Set User Variable](actions/set-user-variable.md) | `POST /vars/set` | [docs](https://smm.targethunter.help/dev/api/methods/vars/set) |
