# <img src="https://images.mindcloud.co/apps/icons/medium-41e3867bd9ed7bc9cddd9531779c81ec_1781290488171.png" alt="CallKeeper logo" width="28" height="28"> CallKeeper: Universal API

AI-powered call management, contact, recording, scheduling, calendar, billing, and speaker-identification API integration for CallKeeper.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/callKeeper/latest
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://callkeeper.ai
- **Vendor API docs:** https://api.callkeeper.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Info](actions/get-current-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Add Party To Call](actions/add-party-to-call.md) | PUT | Updates a call in CallKeeper by adding a party. |
| [Delete Call](actions/delete-call.md) | DELETE | Deletes an existing call from CallKeeper. |
| [Get Active Call](actions/get-active-call.md) | GET | Retrieves the active call from CallKeeper. |
| [Get Call](actions/get-call.md) | GET | Retrieves a specific call from CallKeeper. |
| [Hangup Call](actions/hangup-call.md) | PUT | Updates a call in CallKeeper by hanging up. |
| [Hold Call](actions/hold-call.md) | PUT | Updates a call in CallKeeper by placing it on hold. |
| [Initiate Call](actions/initiate-call.md) | POST | Initiates a new call in CallKeeper. |
| [Initiate Record Me Call](actions/initiate-record-me-call.md) | POST | Initiates a new record-me call in CallKeeper. |
| [Link Contact To Call](actions/link-contact-to-call.md) | PUT | Updates a call in CallKeeper by linking a contact. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from the current CallKeeper account. |
| [Mute Call](actions/mute-call.md) | PUT | Updates a call in CallKeeper by muting it. |
| [Resume Call](actions/resume-call.md) | PUT | Updates a call in CallKeeper by resuming it. |
| [Search Calls](actions/search-calls.md) | GET | Finds calls in CallKeeper by search query. |
| [Transfer Call](actions/transfer-call.md) | PUT | Updates a call in CallKeeper by transferring it. |

### Call Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Stats](actions/get-call-stats.md) | GET | Retrieves call statistics from the current CallKeeper account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in CallKeeper. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from CallKeeper. |
| [Delete Contact Avatar](actions/delete-contact-avatar.md) | DELETE | Deletes a contact avatar from CallKeeper. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a specific contact from CallKeeper. |
| [Get Contact By Phone](actions/get-contact-by-phone.md) | GET | Finds a contact in CallKeeper by phone number. |
| [Import Contacts](actions/import-contacts.md) | POST | Imports contacts into the current CallKeeper account. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from the current CallKeeper account. |
| [List Favorite Contacts](actions/list-favorite-contacts.md) | GET | Retrieves favorite contacts from the current CallKeeper account. |
| [Quick Create Contact](actions/quick-create-contact.md) | POST | Creates a new contact quickly in CallKeeper. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in CallKeeper by search query. |
| [Sync Google Contacts](actions/sync-google-contacts.md) | POST | Syncs Google contacts into the current CallKeeper account. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in CallKeeper. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Delete Recording](actions/delete-recording.md) | DELETE | Deletes an existing recording from CallKeeper. |
| [Download Recording](actions/download-recording.md) | GET | Retrieves downloadable recording content from CallKeeper. |
| [Get Recording](actions/get-recording.md) | GET | Retrieves a specific recording from CallKeeper. |
| [List Recordings](actions/list-recordings.md) | GET | Retrieves recordings from the current CallKeeper account. |
| [Search Recordings](actions/search-recordings.md) | GET | Finds recordings in CallKeeper by search query. |
| [Stream Recording](actions/stream-recording.md) | GET | Retrieves a recording stream from CallKeeper. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Info](actions/get-current-user-info.md) | GET | Retrieves current user information from CallKeeper. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves the current user profile from CallKeeper. |
| [Update Profile](actions/update-profile.md) | PUT | Updates the current user profile in CallKeeper. |

