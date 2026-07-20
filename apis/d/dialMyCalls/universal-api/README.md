# <img src="https://images.mindcloud.co/apps/icons/dial-my-calls_1774541376600.png" alt="DialMyCalls logo" width="28" height="28"> DialMyCalls: Universal API

Send mass texts and calls, manage contacts, and track broadcasts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dialMyCalls/latest
- **Category:** Support / Contact Center
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dialmycalls.com
- **Vendor API docs:** https://www.dialmycalls.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your account details from DialMyCalls. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Call](actions/cancel-call.md) | DELETE | Cancels an existing call in DialMyCalls. |
| [Create Call](actions/create-call.md) | POST | Creates a new call in DialMyCalls. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from DialMyCalls. |
| [List Calls](actions/list-calls.md) | GET | Retrieves a list of calls from DialMyCalls. |

### Caller Id

| Action | Method | Description |
| --- | --- | --- |
| [Add Caller ID](actions/add-caller-id.md) | POST | Creates a new caller ID in DialMyCalls. |
| [Get Caller ID](actions/get-caller-id.md) | GET | Retrieves a caller ID from DialMyCalls. |
| [List Caller IDs](actions/list-caller-ids.md) | GET | Retrieves a list of caller IDs from DialMyCalls. |
| [Update Caller ID](actions/update-caller-id.md) | PUT | Updates an existing caller ID in DialMyCalls. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in DialMyCalls. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from DialMyCalls. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact record from DialMyCalls. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from DialMyCalls. |
| [List Contacts in Group](actions/list-contacts-in-group.md) | GET | Retrieves contacts from a specific DialMyCalls group. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in DialMyCalls. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Group](actions/add-group.md) | POST | Creates a new group in DialMyCalls. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from DialMyCalls. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from DialMyCalls. |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from DialMyCalls. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in DialMyCalls. |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [List Keywords](actions/list-keywords.md) | GET | Retrieves a list of keywords from DialMyCalls. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Create Recording (Text-to-Speech)](actions/create-recording-text-to-speech.md) | POST | Creates a text-to-speech recording in DialMyCalls. |
| [Get Recording](actions/get-recording.md) | GET | Retrieves a recording from DialMyCalls. |
| [List Recordings](actions/list-recordings.md) | GET | Retrieves a list of recordings from DialMyCalls. |

### Text

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Text](actions/cancel-text.md) | DELETE | Cancels an existing text in DialMyCalls. |
| [Create Text](actions/create-text.md) | POST | Creates a new text in DialMyCalls. |
| [Get Text](actions/get-text.md) | GET | Retrieves a text from DialMyCalls. |
| [List Texts](actions/list-texts.md) | GET | Retrieves a list of texts from DialMyCalls. |

### Vanity Number

| Action | Method | Description |
| --- | --- | --- |
| [List Vanity Numbers](actions/list-vanity-numbers.md) | GET | Retrieves available vanity numbers from DialMyCalls. |

