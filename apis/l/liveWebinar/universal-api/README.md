# <img src="https://images.mindcloud.co/apps/icons/live-webinar_1774545508871.png" alt="LiveWebinar logo" width="28" height="28"> LiveWebinar: Universal API

LiveWebinar wrapper for webinar hosting, users, webinars, registrants, participants, presenters, invites, personal rooms, and forms.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/liveWebinar/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.livewebinar.com
- **Vendor API docs:** https://docs.archiebot.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Me](actions/get-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Personal Room](actions/create-personal-room.md) | POST | Creates a personal room in LiveWebinar. |
| [Create Widget](actions/create-widget.md) | POST | Creates a new widget in LiveWebinar. |
| [Create Widget Registrant](actions/create-widget-registrant.md) | POST | Creates a widget registrant in LiveWebinar. |
| [Delete Widget](actions/delete-widget.md) | DELETE | Deletes an existing widget from LiveWebinar. |
| [Get Widget](actions/get-widget.md) | GET | Retrieves a widget from LiveWebinar. |
| [Invite Widget User](actions/invite-widget-user.md) | POST | Invites a user to a widget in LiveWebinar. |
| [List Widget Invites](actions/list-widget-invites.md) | GET | Retrieves widget invites from LiveWebinar. |
| [List Widget Participants](actions/list-widget-participants.md) | GET | Retrieves widget participants from LiveWebinar. |
| [List Widget Presenters](actions/list-widget-presenters.md) | GET | Retrieves widget presenters from LiveWebinar. |
| [List Widget Registrants](actions/list-widget-registrants.md) | GET | Retrieves widget registrants from LiveWebinar. |
| [List Widgets](actions/list-widgets.md) | GET | Retrieves widgets from LiveWebinar. |
| [Update Widget](actions/update-widget.md) | PUT | Updates an existing widget in LiveWebinar. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in LiveWebinar. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from LiveWebinar. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from LiveWebinar. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in LiveWebinar. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in LiveWebinar. |
| [Disable User](actions/disable-user.md) | PUT | Disables a user in LiveWebinar. |
| [Enable User](actions/enable-user.md) | PUT | Enables a user in LiveWebinar. |
| [Get Me](actions/get-me.md) | GET | Retrieves the authenticated user from LiveWebinar. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from LiveWebinar. |
| [List Users](actions/list-users.md) | GET | Retrieves users from LiveWebinar. |
| [Search Users](actions/search-users.md) | GET | Finds users in LiveWebinar. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in LiveWebinar. |

