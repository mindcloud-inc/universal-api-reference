# <img src="https://images.mindcloud.co/apps/icons/dialpad_1773849841570.png" alt="Dialpad logo" width="28" height="28"> Dialpad: Universal API

Manage Dialpad users, calls, messages, and contact center resources

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dialpad/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dialpad.com
- **Vendor API docs:** https://developers.dialpad.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call](actions/get-call.md) | GET | Retrieves detailed information for a concluded call in Dialpad. |
| [Get Call AI Recap](actions/get-call-ai-recap.md) | GET | Retrieves an AI recap for a Dialpad call. |
| [Get Call Transcript](actions/get-call-transcript.md) | GET | Retrieves a Dialpad AI transcript for a call. |
| [Initiate Call](actions/initiate-call.md) | POST | Initiates an outbound call from a Dialpad user. |
| [List Calls](actions/list-calls.md) | GET | Retrieves concluded call records from Dialpad. |
| [Transfer Call](actions/transfer-call.md) | PUT | Transfers a call to another recipient in Dialpad. |

### Call Center

| Action | Method | Description |
| --- | --- | --- |
| [List Call Centers](actions/list-call-centers.md) | GET |  |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Dialpad. |
| [Get Channel](actions/get-channel.md) | GET | Retrieves detailed channel information from Dialpad. |
| [List Channels](actions/list-channels.md) | GET | Retrieves company channel records from Dialpad. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Dialpad. |
| [Create or Update Contact](actions/create-or-update-contact.md) | POST | Creates or updates a contact in Dialpad by unique ID. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves detailed contact information from Dialpad. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves shared or local contacts from Dialpad. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Dialpad. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET |  |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | POST | Creates a new meeting in Dialpad. |
| [Get Meeting](actions/get-meeting.md) | GET | Retrieves detailed meeting information from Dialpad. |
| [List Meetings](actions/list-meetings.md) | GET | Retrieves meetings for a specific Dialpad user. |

### Office

| Action | Method | Description |
| --- | --- | --- |
| [Get Office](actions/get-office.md) | GET | Retrieves detailed office information from Dialpad. |
| [List Offices](actions/list-offices.md) | GET | Retrieves accessible office records from Dialpad. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Numbers](actions/list-numbers.md) | GET | Retrieves company phone numbers from Dialpad. |

### Sms

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS message from Dialpad. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Dialpad. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Dialpad. |
| [Get User](actions/get-user.md) | GET | Retrieves detailed user information from Dialpad. |
| [List Channel Members](actions/list-channel-members.md) | GET | Retrieves members of a Dialpad channel. |
| [List Users](actions/list-users.md) | GET | Retrieves company user records from Dialpad. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Dialpad. |
| [Update User Status](actions/update-user-status.md) | PUT | Updates a user's status in Dialpad. |

