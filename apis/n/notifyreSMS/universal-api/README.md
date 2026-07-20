# <img src="https://images.mindcloud.co/apps/icons/images-11_1774548610248.jpeg" alt="Notifyre SMS logo" width="28" height="28"> Notifyre SMS: Universal API

Send, receive, and manage SMS, MMS, fax, and address book workflows with Notifyre's public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/notifyreSMS/latest
- **Category:** Communication / Team Messaging
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://notifyre.com
- **Vendor API docs:** https://docs.notifyre.com/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download MMS Reply](actions/download-mms-reply.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/download-mms-reply?connectionId=$CONNECTION_ID&replyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Notifyre. |
| [Delete Contacts](actions/delete-contacts.md) | DELETE | Deletes selected contacts from Notifyre address book. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Notifyre address book. |
| [List Contacts](actions/list-contacts.md) | GET | Finds contacts in Notifyre by search filters. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Notifyre. |

### Contact Group Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts To Groups](actions/add-contacts-to-groups.md) | PUT | Adds contacts to groups in Notifyre. |
| [Remove Contacts From Group](actions/remove-contacts-from-group.md) | PUT | Removes contacts from a Notifyre group. |

### Fax

| Action | Method | Description |
| --- | --- | --- |
| [Send Fax](actions/send-fax.md) | POST | Creates a fax message in Notifyre. |

### Fax Cover Page

| Action | Method | Description |
| --- | --- | --- |
| [List Cover Pages](actions/list-cover-pages.md) | GET | Retrieves fax cover pages from Notifyre. |

### Fax Document Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Fax Document Status](actions/get-fax-document-status.md) | GET | Retrieves fax document status from Notifyre. |

### Fax Document Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload Fax Document](actions/upload-fax-document.md) | POST | Uploads a fax document to Notifyre. |

### Fax Number

| Action | Method | Description |
| --- | --- | --- |
| [List Fax Numbers](actions/list-fax-numbers.md) | GET | Retrieves available fax numbers from Notifyre. |

### Fax Price

| Action | Method | Description |
| --- | --- | --- |
| [List Fax Prices](actions/list-fax-prices.md) | GET | Retrieves current fax prices from Notifyre. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Notifyre. |
| [Delete Groups](actions/delete-groups.md) | DELETE | Deletes selected groups from Notifyre address book. |
| [List Groups](actions/list-groups.md) | GET | Retrieves contact groups from the Notifyre address book. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Notifyre. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Sent SMS](actions/get-sent-sms.md) | GET | Retrieves a sent SMS message from Notifyre. |
| [Send SMS](actions/send-sms.md) | POST | Creates an SMS message in Notifyre. |

### Mms Reply Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Download MMS Reply](actions/download-mms-reply.md) | GET | Downloads an MMS reply attachment from Notifyre. |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [List SMS Prices](actions/list-sms-prices.md) | GET | Retrieves current SMS prices from Notifyre. |

### Received Fax

| Action | Method | Description |
| --- | --- | --- |
| [List Received Faxes](actions/list-received-faxes.md) | GET | Retrieves received fax messages from Notifyre. |

### Received Fax Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Download Received Fax](actions/download-received-fax.md) | GET | Downloads a received fax from Notifyre. |

### Sent Fax

| Action | Method | Description |
| --- | --- | --- |
| [List Sent Faxes](actions/list-sent-faxes.md) | GET | Retrieves sent fax messages from Notifyre. |

### Sent Fax Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Download Sent Fax](actions/download-sent-fax.md) | GET | Downloads a sent fax from Notifyre. |

### Sent Sms Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Get Sent SMS Recipient](actions/get-sent-sms-recipient.md) | GET | Retrieves sent SMS recipient details from Notifyre. |

### Sms Reply

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Reply](actions/get-sms-reply.md) | GET | Retrieves an SMS reply from Notifyre. |
| [Get SMS Reply V2](actions/get-sms-reply-v2.md) | GET | Retrieves an SMS reply from Notifyre with V2 fields. |
| [List SMS Replies](actions/list-sms-replies.md) | GET | Retrieves received SMS replies from Notifyre. |

