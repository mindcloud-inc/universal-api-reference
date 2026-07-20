# <img src="https://images.mindcloud.co/apps/icons/recallai_1775827276961.png" alt="Recallai logo" width="28" height="28"> Recallai: Universal API

Capture Recall.ai meeting bots, recordings, transcripts, calendars, and related workspace resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recallai/latest
- **Category:** Communication / Video Communications
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.recall.ai
- **Vendor API docs:** https://docs.recall.ai/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bots](actions/list-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST | Creates a new bot in Recallai. |
| [Delete Scheduled Bot](actions/delete-scheduled-bot.md) | DELETE | Deletes a scheduled bot from Recallai. |
| [Get Bot](actions/get-bot.md) | GET | Retrieves a bot from Recallai. |
| [List Bots](actions/list-bots.md) | GET | Retrieves bots from Recallai. |
| [Update Scheduled Bot](actions/update-scheduled-bot.md) | PUT | Updates a scheduled bot in Recallai. |

### Bot Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [List Bot Screenshots](actions/list-bot-screenshots.md) | GET | Retrieves bot screenshots from Recallai by bot ID. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | POST | Creates a new calendar in Recallai. |
| [Delete Calendar](actions/delete-calendar.md) | DELETE | Deletes an existing calendar from Recallai. |
| [Get Calendar](actions/get-calendar.md) | GET | Retrieves a calendar from Recallai. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendars from Recallai. |
| [Update Calendar](actions/update-calendar.md) | PUT | Updates an existing calendar in Recallai. |

### Calendar Event

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Events](actions/list-calendar-events.md) | GET | Retrieves calendar events from Recallai. |

### Google Login

| Action | Method | Description |
| --- | --- | --- |
| [Create Google Login](actions/create-google-login.md) | POST | Creates a new Google login in Recallai. |
| [Delete Google Login](actions/delete-google-login.md) | DELETE | Deletes an existing Google login from Recallai. |
| [Get Google Login](actions/get-google-login.md) | GET | Retrieves a Google login from Recallai. |
| [List Google Logins](actions/list-google-logins.md) | GET | Retrieves Google logins from Recallai. |
| [Update Google Login](actions/update-google-login.md) | PUT | Updates an existing Google login in Recallai. |

### Google Login Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Google Login Group](actions/create-google-login-group.md) | POST | Creates a new Google login group in Recallai. |
| [Delete Google Login Group](actions/delete-google-login-group.md) | DELETE | Deletes a Google login group from Recallai. |
| [Get Google Login Group](actions/get-google-login-group.md) | GET | Retrieves a Google login group from Recallai. |
| [List Google Login Groups](actions/list-google-login-groups.md) | GET | Retrieves Google login groups from Recallai. |
| [Update Google Login Group](actions/update-google-login-group.md) | PUT | Updates a Google login group in Recallai. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [List Recordings](actions/list-recordings.md) | GET | Retrieves recordings from Recallai. |

### Sdk Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Desktop SDK Upload](actions/create-desktop-sdk-upload.md) | POST | Creates a desktop SDK upload in Recallai. |
| [Get Desktop SDK Upload](actions/get-desktop-sdk-upload.md) | GET | Retrieves a desktop SDK upload from Recallai. |
| [List Desktop SDK Uploads](actions/list-desktop-sdk-uploads.md) | GET | Retrieves desktop SDK uploads from Recallai. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves usage details from Recallai. |

### Zoom Oauth App

| Action | Method | Description |
| --- | --- | --- |
| [Create Zoom OAuth App](actions/create-zoom-o-auth-app.md) | POST | Creates a new Zoom OAuth app in Recallai. |
| [Delete Zoom OAuth App](actions/delete-zoom-o-auth-app.md) | DELETE | Deletes an existing Zoom OAuth app from Recallai. |
| [Get Zoom OAuth App](actions/get-zoom-o-auth-app.md) | GET | Retrieves a Zoom OAuth app from Recallai. |
| [List Zoom OAuth Apps](actions/list-zoom-o-auth-apps.md) | GET | Retrieves Zoom OAuth apps from Recallai. |
| [Update Zoom OAuth App](actions/update-zoom-o-auth-app.md) | PUT | Updates an existing Zoom OAuth app in Recallai. |

