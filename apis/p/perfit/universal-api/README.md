# <img src="https://images.mindcloud.co/apps/icons/images_1773938117618.jpeg" alt="Perfit logo" width="28" height="28"> Perfit: Universal API

Manage contacts, audiences, and email activity in Perfit

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/perfit/latest
- **Category:** Marketing
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://perfit.com/es
- **Vendor API docs:** https://developers.myperfit.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Account Activity](actions/list-account-activity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/list-account-activity?connectionId=$CONNECTION_ID&account=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Account Activity](actions/list-account-activity.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Interest To Contact](actions/add-interest-to-contact.md) | PUT |  |
| [Create Or Update Contact In List](actions/create-or-update-contact-in-list.md) | POST |  |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | PUT |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Custom Trigger Event](actions/send-custom-trigger-event.md) | POST |  |

### Interest

| Action | Method | Description |
| --- | --- | --- |
| [Create Interest](actions/create-interest.md) | POST |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |

