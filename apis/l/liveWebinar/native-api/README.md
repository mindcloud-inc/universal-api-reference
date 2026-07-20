# LiveWebinar: Native API Reference

A consolidated summary of LiveWebinar's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.archiebot.com/
- **API base URL:** `https://api.archiebot.com`

## Authentication

### OAuth2 Password Grant

ArchieBot OAuth token flow using per-user client credentials plus username and password.

### Credentials

- **Username or Email:** `username` · required · The ArchieBot or LiveWebinar username or email used for OAuth login.
- **Password:** `password` · required · The password for the ArchieBot or LiveWebinar user account.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.archiebot.com/api/oauth/access_token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.archiebot.com/api/oauth/access_token/refresh. A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.archiebot.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.archiebot.v1+json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | `POST api/forms` | [docs](https://docs.archiebot.com/?version=latest#534d2dc7-def5-41c6-af8c-df87e2c8c9d9) |
| [Create Personal Room](actions/create-personal-room.md) | `POST api/widgets/:widget_id/personal` | [docs](https://docs.archiebot.com/?version=latest#739a2b58-c457-4d88-8ec0-94589f2e5180) |
| [Create User](actions/create-user.md) | `POST api/users` | [docs](https://docs.archiebot.com/?version=latest#bac4389f-4fde-4fe7-a945-f82f745bbb12) |
| [Create Widget](actions/create-widget.md) | `POST api/widgets` | [docs](https://docs.archiebot.com/?version=latest#e1cec9d4-d582-47c3-a978-40041f6c1026) |
| [Create Widget Registrant](actions/create-widget-registrant.md) | `POST api/widgets/:widget_id/registrants` | [docs](https://docs.archiebot.com/?version=latest#dedea85d-27bf-4492-81ed-b089baba4be7) |
| [Delete Widget](actions/delete-widget.md) | `DELETE api/widgets/:widget_id` | [docs](https://docs.archiebot.com/?version=latest#c396a1bd-1a6b-41c2-be05-b040039b6772) |
| [Disable User](actions/disable-user.md) | `PUT api/users/:user_id/disable` | [docs](https://docs.archiebot.com/?version=latest#3adc1168-5ce6-4ce0-8225-02216700836e) |
| [Enable User](actions/enable-user.md) | `PUT api/users/:user_id/enable` | [docs](https://docs.archiebot.com/?version=latest#4ba74735-17cf-4cf9-ba39-5d5ef57bbf57) |
| [Get Form](actions/get-form.md) | `GET api/forms/:form_id` | [docs](https://docs.archiebot.com/?version=latest#c2c06c06-0299-4a1c-b657-db92bdfd734b) |
| [Get Me](actions/get-me.md) | `GET api/me` | [docs](https://docs.archiebot.com/?version=latest#6104b6f9-573f-4abf-84de-4c2874ef678b) |
| [Get User](actions/get-user.md) | `GET api/users/:user_id` | [docs](https://docs.archiebot.com/?version=latest#bf5891d0-4cbe-4881-9c47-57908db911e8) |
| [Get Widget](actions/get-widget.md) | `GET api/widgets/:widget_id` | [docs](https://docs.archiebot.com/?version=latest#8d7727a4-b209-41ab-957b-73096c7fb2fd) |
| [Invite Widget User](actions/invite-widget-user.md) | `POST api/widgets/:widget_id/invites/invite` | [docs](https://docs.archiebot.com/?version=latest#2224d9bd-cc10-4718-9428-eea4aab5e6fa) |
| [List Forms](actions/list-forms.md) | `GET api/forms` | [docs](https://docs.archiebot.com/?version=latest#4bce4aa7-9228-4819-a0bb-c00910c1c773) |
| [List Users](actions/list-users.md) | `GET api/users` | [docs](https://docs.archiebot.com/?version=latest#234d7e59-b507-4ff5-8934-249996a92fa5) |
| [List Widget Invites](actions/list-widget-invites.md) | `GET api/widgets/:widget_id/invites` | [docs](https://docs.archiebot.com/?version=latest#2844041d-d819-4a9a-bb89-92ce4015843a) |
| [List Widget Participants](actions/list-widget-participants.md) | `GET api/widgets/:widget_id/participants` | [docs](https://docs.archiebot.com/?version=latest#8ceca65c-bb33-4443-841d-ee1a72258fe9) |
| [List Widget Presenters](actions/list-widget-presenters.md) | `GET api/widgets/:widget_id/presenters` | [docs](https://docs.archiebot.com/?version=latest#a58dfbb8-391f-4dd1-bb5a-3d6488949d54) |
| [List Widget Registrants](actions/list-widget-registrants.md) | `GET api/widgets/:widget_id/registrants` | [docs](https://docs.archiebot.com/?version=latest#bcc8b4af-2ba7-42ee-a23b-422b13bddbc3) |
| [List Widgets](actions/list-widgets.md) | `GET api/widgets` | [docs](https://docs.archiebot.com/?version=latest#4e9e6299-a0c1-46c6-afbb-fd5efbf039e2) |
| [Search Users](actions/search-users.md) | `GET api/users/search` | [docs](https://docs.archiebot.com/?version=latest#97e7bfe0-8160-4760-8d3a-05219ed4ba4b) |
| [Update Form](actions/update-form.md) | `PUT api/forms/:form_id` | [docs](https://docs.archiebot.com/?version=latest#4cabfd02-9151-45f8-8825-3c8976e1ab07) |
| [Update User](actions/update-user.md) | `PUT api/users/:user_id` | [docs](https://docs.archiebot.com/?version=latest#4414eb9b-a67e-4146-9a47-8fde3e97ad84) |
| [Update Widget](actions/update-widget.md) | `PUT api/widgets/:widget_id` | [docs](https://docs.archiebot.com/?version=latest#4da1cafc-f286-46d9-9ea2-b19441722d01) |
