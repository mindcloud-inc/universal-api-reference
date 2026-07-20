# Communi App: Native API Reference

A consolidated summary of Communi App's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://api.communiapp.de/docs
- **OpenAPI specification:** https://api.communiapp.de/docs/yaml
- **API base URL:** `https://api.communiapp.de`

## Authentication

### API Token

Use the CommuniApp REST API access token from Admin -> Integration -> REST-API. The token is sent in the X-Authorization header with the required Bearer prefix.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.communiapp.de/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Article](actions/get-article.md) | `GET /rest/article/:id` | [docs](https://api.communiapp.de/docs#/Article/get_rest_article__id_) |
| [Get Conversation](actions/get-conversation.md) | `GET /rest/conversation/:id` | [docs](https://api.communiapp.de/docs#/Conversation/get_rest_conversation__id_) |
| [Get Custom Page](actions/get-custom-page.md) | `GET /rest/customPage/:id` | [docs](https://api.communiapp.de/docs#/CustomPage/get_rest_customPage__id_) |
| [Get Donation](actions/get-donation.md) | `GET /rest/donation/:id` | [docs](https://api.communiapp.de/docs#/Donation/get_rest_donation__id_) |
| [Get Event](actions/get-event.md) | `GET /rest/event/:id` | [docs](https://api.communiapp.de/docs#/Event/get_rest_event__id_) |
| [Get Group](actions/get-group.md) | `GET /rest/group/:id` | [docs](https://api.communiapp.de/docs#/Group/get_rest_group__id_) |
| [Get Login Status](actions/get-login-status.md) | `GET /rest/login` | [docs](https://api.communiapp.de/docs#/Login/get_rest_login) |
| [Get Message](actions/get-message.md) | `GET /rest/message/:id` | [docs](https://api.communiapp.de/docs#/Message/get_rest_message__id_) |
| [Get Offer](actions/get-offer.md) | `GET /rest/offer/:id` | [docs](https://api.communiapp.de/docs#/Offer/get_rest_offer__id_) |
| [Get Poll](actions/get-poll.md) | `GET /rest/poll/:id` | [docs](https://api.communiapp.de/docs#/Poll/get_rest_poll__id_) |
| [Get Quest](actions/get-quest.md) | `GET /rest/quest/:id` | [docs](https://api.communiapp.de/docs#/Quest/get_rest_quest__id_) |
| [Get Recommendation](actions/get-recommendation.md) | `GET /rest/recommendation/:id` | [docs](https://api.communiapp.de/docs#/Recommendation/get_rest_recommendation__id_) |
| [Get User](actions/get-user.md) | `GET /rest/user/:id` | [docs](https://api.communiapp.de/docs#/User/get_rest_user__id_) |
| [Get User Conversation](actions/get-user-conversation.md) | `GET /rest/userConversation/:id` | [docs](https://api.communiapp.de/docs#/UserConversation/get_rest_userConversation__id_) |
| [Get User Group](actions/get-user-group.md) | `GET /rest/userGroup/:id` | [docs](https://api.communiapp.de/docs#/UserGroup/get_rest_userGroup__id_) |
| [Get User Poll Answer](actions/get-user-poll-answer.md) | `GET /rest/userPollAnswer/:id` | [docs](https://api.communiapp.de/docs#/UserPollAnswer/get_rest_userPollAnswer__id_) |
| [List Articles](actions/list-articles.md) | `GET /rest/article` | [docs](https://api.communiapp.de/docs#/Article/get_rest_article) |
| [List Custom Pages](actions/list-custom-pages.md) | `GET /rest/customPage` | [docs](https://api.communiapp.de/docs#/CustomPage/get_rest_customPage) |
| [List Donations](actions/list-donations.md) | `GET /rest/donation` | [docs](https://api.communiapp.de/docs#/Donation/get_rest_donation) |
| [List Events](actions/list-events.md) | `GET /rest/event` | [docs](https://api.communiapp.de/docs#/Event/get_rest_event) |
| [List Groups](actions/list-groups.md) | `GET /rest/group` | [docs](https://api.communiapp.de/docs#/Group/get_rest_group) |
| [List Messages](actions/list-messages.md) | `GET /rest/message` | [docs](https://api.communiapp.de/docs#/Message/get_rest_message) |
| [List Offers](actions/list-offers.md) | `GET /rest/offer` | [docs](https://api.communiapp.de/docs#/Offer/get_rest_offer) |
| [List Polls](actions/list-polls.md) | `GET /rest/poll` | [docs](https://api.communiapp.de/docs#/Poll/get_rest_poll) |
| [List Quests](actions/list-quests.md) | `GET /rest/quest` | [docs](https://api.communiapp.de/docs#/Quest/get_rest_quest) |
| [List Recommendations](actions/list-recommendations.md) | `GET /rest/recommendation` | [docs](https://api.communiapp.de/docs#/Recommendation/get_rest_recommendation) |
| [List Statistics](actions/list-statistics.md) | `GET /rest/statistic` | [docs](https://api.communiapp.de/docs#/Statistic/get_rest_statistic) |
| [List User Conversations](actions/list-user-conversations.md) | `GET /rest/userConversation` | [docs](https://api.communiapp.de/docs#/UserConversation/get_rest_userConversation) |
| [List User Groups](actions/list-user-groups.md) | `GET /rest/userGroup` | [docs](https://api.communiapp.de/docs#/UserGroup/get_rest_userGroup) |
| [List User Poll Answers](actions/list-user-poll-answers.md) | `GET /rest/userPollAnswer` | [docs](https://api.communiapp.de/docs#/UserPollAnswer/get_rest_userPollAnswer) |
| [List Users](actions/list-users.md) | `GET /rest/user` | [docs](https://api.communiapp.de/docs#/User/get_rest_user) |
