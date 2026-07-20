# <img src="https://images.mindcloud.co/apps/icons/trust-icon_1775506709109.png" alt="Trust logo" width="28" height="28"> Trust: Universal API

Trust Public API for workspaces, campaigns, contacts, media uploads, testimonials, and widgets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trust/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://usetrust.io
- **Vendor API docs:** https://api-docs.usetrust.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from a Trust workspace. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Trust. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Trust. |
| [Find Contact By Email](actions/find-contact-by-email.md) | GET | Finds contacts in Trust by email address. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Trust. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a Trust workspace. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Trust. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Assign Testimonial To Widget](actions/assign-testimonial-to-widget.md) | PUT | Assigns a testimonial to a Trust widget. |
| [Create Testimonial](actions/create-testimonial.md) | POST | Creates a new testimonial in Trust. |
| [Delete Testimonial](actions/delete-testimonial.md) | DELETE | Deletes an existing testimonial from Trust. |
| [Get Testimonial](actions/get-testimonial.md) | GET | Retrieves a testimonial from Trust. |
| [List Testimonials](actions/list-testimonials.md) | GET | Retrieves testimonials from a Trust workspace. |
| [List Widgets](actions/list-widgets.md) | GET | Retrieves testimonial widgets from Trust. |
| [Remove Testimonial From Widget](actions/remove-testimonial-from-widget.md) | PUT | Removes a testimonial from a Trust widget. |
| [Update Testimonial](actions/update-testimonial.md) | PUT | Updates an existing testimonial in Trust. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload Contact Image](actions/upload-contact-image.md) | POST | Uploads a testimonial image to Trust. |
| [Upload Media Image](actions/upload-media-image.md) | POST | Uploads an image for the Trust video editor. |
| [Upload Small Video](actions/upload-small-video.md) | POST | Uploads a small testimonial video to Trust. |
| [Upload Video](actions/upload-video.md) | POST | Uploads a testimonial video to Trust. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Trust. |

