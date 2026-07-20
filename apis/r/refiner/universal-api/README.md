# <img src="https://images.mindcloud.co/apps/icons/refiner_1774044610976.png" alt="Refiner logo" width="28" height="28"> Refiner: Universal API

Create surveys, collect responses, and analyze customer feedback

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/refiner/latest
- **Category:** Marketing
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://refiner.io
- **Vendor API docs:** https://refiner.io/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves information about your Refiner account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Refiner by ID or email. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Refiner by ID or email. |
| [Identify User](actions/identify-user.md) | POST | Creates or updates a user in Refiner. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Refiner account. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Track Event](actions/track-event.md) | POST | Tracks a user event in Refiner. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Delete Form](actions/delete-form.md) | DELETE | Archives an existing form in Refiner. |
| [Duplicate Form](actions/duplicate-form.md) | POST | Creates a duplicate of a form in Refiner. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from your Refiner account. |
| [Publish Form](actions/publish-form.md) | PUT | Publishes or unpublishes a form in Refiner. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Reporting](actions/get-reporting.md) | GET | Retrieves survey reporting data from Refiner. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [List Responses](actions/list-responses.md) | GET | Retrieves survey views and responses from Refiner. |
| [Store Responses](actions/store-responses.md) | POST | Stores survey response data in Refiner. |
| [Tag Responses](actions/tag-responses.md) | PUT | Updates tags on survey responses in Refiner. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Segment](actions/add-user-to-segment.md) | POST | Adds a user to a manual segment in Refiner. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from your Refiner account. |
| [Remove User from Segment](actions/remove-user-from-segment.md) | DELETE | Removes a user from a manual segment in Refiner. |

