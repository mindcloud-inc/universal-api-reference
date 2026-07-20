# <img src="https://images.mindcloud.co/apps/icons/ring-central-icon_1782394384150.png" alt="RingCentral logo" width="28" height="28"> RingCentral: Universal API

RingCentral through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ringCentral/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves the current RingCentral account information. |

### Call Log

| Action | Method | Description |
| --- | --- | --- |
| [List Company Call Records](actions/list-company-call-records.md) | GET | Returns call log records filtered by parameters specified. |
| [List User Call Records](actions/list-user-call-records.md) | GET | Returns call log records filtered by parameters specified. |

### Call Queue

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Queue](actions/get-call-queue.md) | GET | Retrieves a call queue from a RingCentral account. |
| [List Call Queues](actions/list-call-queues.md) | GET | Retrieves call queues from a RingCentral account. |

### Call Recording

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Recording](actions/get-call-recording.md) | GET | Returns call recordings by ID(s). |
| [Get Call Recording Content](actions/get-call-recording-content.md) | GET | Returns media content of a call recording (audio/mpeg or audio/wav) |

### Extension

| Action | Method | Description |
| --- | --- | --- |
| [Get Extension](actions/get-extension.md) | GET | Retrieves an extension from a RingCentral account. |
| [List Extensions](actions/list-extensions.md) | GET | Retrieves extensions from a RingCentral account. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from a RingCentral extension. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from a RingCentral extension. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from a RingCentral extension. |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS message from a RingCentral extension. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Company Phone Numbers](actions/list-company-phone-numbers.md) | GET | Retrieves company phone numbers from RingCentral. |
| [List Extension Phone Numbers](actions/list-extension-phone-numbers.md) | GET | Retrieves phone numbers for a RingCentral extension. |

