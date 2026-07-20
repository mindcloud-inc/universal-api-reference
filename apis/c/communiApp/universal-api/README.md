# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-27-154042_1774636904299.png" alt="Communi App logo" width="28" height="28"> Communi App: Universal API

CommuniApp is a community platform for managing events, announcements, recommendations, offers, quests, polls, messaging, groups, and donations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/communiApp/latest
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://communiapp.de
- **Vendor API docs:** https://api.communiapp.de/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-events?connectionId=$CONNECTION_ID&group=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Get Article](actions/get-article.md) | GET |  |
| [List Articles](actions/list-articles.md) | GET |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [List User Conversations](actions/list-user-conversations.md) | GET |  |

### Custom Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Page](actions/get-custom-page.md) | GET |  |
| [List Custom Pages](actions/list-custom-pages.md) | GET |  |

### Donation

| Action | Method | Description |
| --- | --- | --- |
| [Get Donation](actions/get-donation.md) | GET |  |
| [List Donations](actions/list-donations.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |

### Login Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Login Status](actions/get-login-status.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET |  |
| [List Messages](actions/list-messages.md) | GET |  |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Get Offer](actions/get-offer.md) | GET |  |
| [List Offers](actions/list-offers.md) | GET |  |

### Poll

| Action | Method | Description |
| --- | --- | --- |
| [Get Poll](actions/get-poll.md) | GET |  |
| [List Polls](actions/list-polls.md) | GET |  |

### Quest

| Action | Method | Description |
| --- | --- | --- |
| [Get Quest](actions/get-quest.md) | GET |  |
| [List Quests](actions/list-quests.md) | GET |  |

### Recommendation

| Action | Method | Description |
| --- | --- | --- |
| [Get Recommendation](actions/get-recommendation.md) | GET |  |
| [List Recommendations](actions/list-recommendations.md) | GET |  |

### Statistic

| Action | Method | Description |
| --- | --- | --- |
| [List Statistics](actions/list-statistics.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### User Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get User Conversation](actions/get-user-conversation.md) | GET |  |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [Get User Group](actions/get-user-group.md) | GET |  |
| [List User Groups](actions/list-user-groups.md) | GET |  |

### User Poll Answer

| Action | Method | Description |
| --- | --- | --- |
| [Get User Poll Answer](actions/get-user-poll-answer.md) | GET |  |
| [List User Poll Answers](actions/list-user-poll-answers.md) | GET |  |

