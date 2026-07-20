# <img src="https://images.mindcloud.co/apps/icons/tidio_1773250944716.png" alt="Tidio logo" width="28" height="28"> Tidio: Universal API

Manage contacts, tickets, products, and Lyro support workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tidio/latest
- **Category:** Support / Contact Center
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tidio.com/
- **Vendor API docs:** https://developers.tidio.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact Messages [Plus plan]](actions/get-contact-messages-plus-plan.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-messages-plus-plan?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts [Plus plan]](actions/list-contacts-plus-plan.md) | GET | Retrieves contacts from the Tidio workspace. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact [Plus plan]](actions/create-contact-plus-plan.md) | POST | Creates a contact in the Tidio workspace. |
| [Create Multiple Contacts [Plus plan]](actions/create-multiple-contacts-plus-plan.md) | POST | Creates multiple contacts in the Tidio workspace. |
| [Delete Contact [Plus plan]](actions/delete-contact-plus-plan.md) | DELETE | Deletes a contact from the Tidio workspace. |
| [Get Contact [Plus plan]](actions/get-contact-plus-plan.md) | GET | Retrieves a contact from the Tidio workspace. |
| [Update Contact Properties [Plus plan]](actions/update-contact-properties-plus-plan.md) | PUT | Updates a contact in the Tidio workspace. |
| [Update Multiple Contacts [Plus plan]](actions/update-multiple-contacts-plus-plan.md) | PUT | Updates multiple contacts in the Tidio workspace. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Properties [Plus plan]](actions/list-contact-properties-plus-plan.md) | GET | Retrieves custom contact properties from Tidio. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Add Website as Lyro Data Source [Plus plan]](actions/add-website-as-lyro-data-source-plus-plan.md) | POST | Adds a website as a Lyro data source in Tidio. |
| [Create Lyro QA Data Source [Plus plan]](actions/create-lyro-qa-data-source-plus-plan.md) | POST | Creates a Lyro QA data source in Tidio. |
| [Upsert Lyro Data Source [Plus plan]](actions/upsert-lyro-data-source-plus-plan.md) | PUT | Upserts a Lyro website data source in Tidio. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [List Departments [Plus plan]](actions/list-departments-plus-plan.md) | GET | Retrieves departments from the Tidio workspace. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Messages [Plus plan]](actions/get-contact-messages-plus-plan.md) | GET | Retrieves messages for a contact from Tidio. |
| [Reply to Ticket [Plus plan]](actions/reply-to-ticket-plus-plan.md) | POST | Replies to a ticket in the Tidio workspace. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Viewed Pages History [Plus plan]](actions/get-viewed-pages-history-plus-plan.md) | GET | Retrieves viewed page history for a contact in Tidio. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from the Tidio product catalog. |
| [Upsert Products](actions/upsert-products.md) | PUT | Upserts products in the Tidio product catalog. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Info [Plus plan]](actions/get-project-info-plus-plan.md) | GET | Retrieves project information from the Tidio workspace. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Ask Lyro [Plus plan]](actions/ask-lyro-plus-plan.md) | POST | Asks Lyro to answer a ticket in Tidio. |
| [Create Ticket (As Contact) [Plus plan]](actions/create-ticket-as-contact-plus-plan.md) | POST | Creates a ticket as a contact in Tidio. |
| [Delete Ticket [Plus plan]](actions/delete-ticket-plus-plan.md) | DELETE | Deletes a ticket from the Tidio workspace. |
| [Get Ticket Details [Plus plan]](actions/get-ticket-details-plus-plan.md) | GET | Retrieves ticket details from the Tidio workspace. |
| [List Tickets [Plus plan]](actions/list-tickets-plus-plan.md) | GET | Retrieves tickets from the Tidio workspace. |
| [Update Ticket [Plus plan]](actions/update-ticket-plus-plan.md) | PUT | Updates a ticket in the Tidio workspace. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Operators [Plus plan]](actions/list-operators-plus-plan.md) | GET | Retrieves operators from the Tidio workspace. |

