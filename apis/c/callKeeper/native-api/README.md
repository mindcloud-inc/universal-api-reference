# CallKeeper: Native API Reference

A consolidated summary of CallKeeper's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://api.callkeeper.ai/docs
- **OpenAPI specification:** https://api.callkeeper.ai/openapi.json
- **API base URL:** `https://api.callkeeper.ai`

## Authentication

### Bearer token

Use a CallKeeper access token from POST /auth/login as a bearer token in the Authorization header.

### Credentials

- **Refresh Token:** `refreshToken` · required · Refresh token returned by POST /auth/login for minting a future access token.
- **User ID:** `userId` · optional · CallKeeper user ID associated with the token.
- **Twilio Phone Number:** `twilioPhoneNumber` · optional · Provisioned CallKeeper Twilio phone number for the account.
- **Access Token:** `accessToken` · required · Bearer access token returned by POST /auth/login.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://api.callkeeper.ai/docs#/Authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Party To Call](actions/add-party-to-call.md) | `POST /calls/:call_id/add-party` | [docs](https://api.callkeeper.ai/docs#/Calls/add_party_to_call_calls__call_id__add_party_post) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api.callkeeper.ai/docs#/Contacts/create_contact_contacts_post) |
| [Delete Call](actions/delete-call.md) | `DELETE /calls/:call_id` | [docs](https://api.callkeeper.ai/docs#/Calls/delete_call_calls__call_id__delete) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contact_id` | [docs](https://api.callkeeper.ai/docs#/Contacts/delete_contact_contacts__contact_id__delete) |
| [Delete Contact Avatar](actions/delete-contact-avatar.md) | `DELETE /contacts/:contact_id/avatar` | [docs](https://api.callkeeper.ai/docs#/Contacts/delete_contact_avatar_contacts__contact_id__avatar_delete) |
| [Delete Recording](actions/delete-recording.md) | `DELETE /recordings/:recording_id` | [docs](https://api.callkeeper.ai/docs#/Recordings/delete_recording_recordings__recording_id__delete) |
| [Download Recording](actions/download-recording.md) | `GET /recordings/:recording_id/download` | [docs](https://api.callkeeper.ai/docs#/Recordings/download_recording_recordings__recording_id__download_get) |
| [Get Active Call](actions/get-active-call.md) | `GET /calls/active` | [docs](https://api.callkeeper.ai/docs#/Calls/get_active_call_calls_active_get) |
| [Get Call](actions/get-call.md) | `GET /calls/:call_id` | [docs](https://api.callkeeper.ai/docs#/Calls/get_call_calls__call_id__get) |
| [Get Call Stats](actions/get-call-stats.md) | `GET /calls/stats` | [docs](https://api.callkeeper.ai/docs#/Calls/get_call_stats_calls_stats_get) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://api.callkeeper.ai/docs#/Contacts/get_contact_contacts__contact_id__get) |
| [Get Contact By Phone](actions/get-contact-by-phone.md) | `GET /contacts/by-phone/:phone` | [docs](https://api.callkeeper.ai/docs#/Contacts/get_contact_by_phone_contacts_by_phone__phone__get) |
| [Get Current User Info](actions/get-current-user-info.md) | `GET /auth/me` | [docs](https://api.callkeeper.ai/docs#/Authentication/get_current_user_info_auth_me_get) |
| [Get Profile](actions/get-profile.md) | `GET /users/profile` | [docs](https://api.callkeeper.ai/docs#/Users/get_profile_users_profile_get) |
| [Get Recording](actions/get-recording.md) | `GET /recordings/:recording_id` | [docs](https://api.callkeeper.ai/docs#/Recordings/get_recording_recordings__recording_id__get) |
| [Hangup Call](actions/hangup-call.md) | `POST /calls/:call_id/hangup` | [docs](https://api.callkeeper.ai/docs#/Calls/hangup_call_calls__call_id__hangup_post) |
| [Hold Call](actions/hold-call.md) | `POST /calls/:call_id/hold` | [docs](https://api.callkeeper.ai/docs#/Calls/hold_call_calls__call_id__hold_post) |
| [Import Contacts](actions/import-contacts.md) | `POST /contacts/import` | [docs](https://api.callkeeper.ai/docs#/Contacts/import_contacts_contacts_import_post) |
| [Initiate Call](actions/initiate-call.md) | `POST /calls` | [docs](https://api.callkeeper.ai/docs#/Calls/initiate_call_calls_post) |
| [Initiate Record Me Call](actions/initiate-record-me-call.md) | `POST /calls/record-me` | [docs](https://api.callkeeper.ai/docs#/Calls/initiate_record_me_call_calls_record_me_post) |
| [Link Contact To Call](actions/link-contact-to-call.md) | `PUT /calls/:call_id/link-contact` | [docs](https://api.callkeeper.ai/docs#/Calls/link_contact_to_call_calls__call_id__link_contact_put) |
| [List Calls](actions/list-calls.md) | `GET /calls` | [docs](https://api.callkeeper.ai/docs#/Calls/list_calls_calls_get) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.callkeeper.ai/docs#/Contacts/list_contacts_contacts_get) |
| [List Favorite Contacts](actions/list-favorite-contacts.md) | `GET /contacts/favorites` | [docs](https://api.callkeeper.ai/docs#/Contacts/list_favorite_contacts_contacts_favorites_get) |
| [List Recordings](actions/list-recordings.md) | `GET /recordings` | [docs](https://api.callkeeper.ai/docs#/Recordings/list_recordings_recordings_get) |
| [Mute Call](actions/mute-call.md) | `POST /calls/:call_id/mute` | [docs](https://api.callkeeper.ai/docs#/Calls/mute_call_calls__call_id__mute_post) |
| [Quick Create Contact](actions/quick-create-contact.md) | `POST /contacts/quick` | [docs](https://api.callkeeper.ai/docs#/Contacts/quick_create_contact_contacts_quick_post) |
| [Resume Call](actions/resume-call.md) | `POST /calls/:call_id/resume` | [docs](https://api.callkeeper.ai/docs#/Calls/resume_call_calls__call_id__resume_post) |
| [Search Calls](actions/search-calls.md) | `GET /calls/search` | [docs](https://api.callkeeper.ai/docs#/Calls/search_calls_calls_search_get) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts/search` | [docs](https://api.callkeeper.ai/docs#/Contacts/search_contacts_contacts_search_get) |
| [Search Recordings](actions/search-recordings.md) | `GET /recordings/search` | [docs](https://api.callkeeper.ai/docs#/Recordings/search_recordings_recordings_search_get) |
| [Stream Recording](actions/stream-recording.md) | `GET /recordings/:recording_id/stream` | [docs](https://api.callkeeper.ai/docs#/Recordings/stream_recording_recordings__recording_id__stream_get) |
| [Sync Google Contacts](actions/sync-google-contacts.md) | `POST /contacts/sync/google` | [docs](https://api.callkeeper.ai/docs#/Contacts/sync_google_contacts_contacts_sync_google_post) |
| [Transfer Call](actions/transfer-call.md) | `POST /calls/:call_id/transfer` | [docs](https://api.callkeeper.ai/docs#/Calls/transfer_call_calls__call_id__transfer_post) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://api.callkeeper.ai/docs#/Contacts/update_contact_contacts__contact_id__put) |
| [Update Profile](actions/update-profile.md) | `PUT /users/profile` | [docs](https://api.callkeeper.ai/docs#/Users/update_profile_users_profile_put) |
