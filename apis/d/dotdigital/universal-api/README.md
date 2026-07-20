# <img src="https://images.mindcloud.co/apps/icons/original_1773689967167.png" alt="Dotdigital logo" width="28" height="28"> Dotdigital: Universal API

Manage contacts, campaigns, and cross-channel marketing automation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dotdigital/latest
- **Category:** Marketing
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dotdigital.com/
- **Vendor API docs:** https://developer.dotdigital.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves account status information from Dotdigital. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Dotdigital. |
| [Get All Campaigns With Filters](actions/get-all-campaigns-with-filters.md) | GET | Retrieves campaigns from Dotdigital with optional filters. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Dotdigital by ID. |
| [Get Campaign Summary](actions/get-campaign-summary.md) | GET | Retrieves campaign reporting summary information from Dotdigital. |
| [Get Campaign With Details](actions/get-campaign-with-details.md) | GET | Retrieves a campaign and its details from Dotdigital. |

### Campaign Send

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Send Status](actions/get-campaign-send-status.md) | GET | Retrieves a campaign send status from Dotdigital by send ID. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contacts Based on Your Criteria](actions/get-contacts-based-on-your-criteria.md) | GET | Finds contacts in Dotdigital by selected criteria. |
| [Retrieve a Contact by an Identifier](actions/retrieve-a-contact-by-an-identifier.md) | GET | Retrieves a contact from Dotdigital by a specified identifier. |

### Contact Data Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Data Fields](actions/get-contact-data-fields.md) | GET | Retrieves contact data fields from Dotdigital. |

### Custom Identifier

| Action | Method | Description |
| --- | --- | --- |
| [Get All Custom Identifiers](actions/get-all-custom-identifiers.md) | GET | Retrieves custom identifiers defined in Dotdigital. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form by ID](actions/get-form-by-id.md) | GET | Retrieves a form from Dotdigital by ID. |
| [Get Forms](actions/get-forms.md) | GET | Retrieves all account forms from Dotdigital. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Dotdigital by ID. |
| [Get Lists](actions/get-lists.md) | GET | Retrieves all available lists from Dotdigital. |
| [Get Private Lists](actions/get-private-lists.md) | GET | Retrieves all private lists from Dotdigital. |
| [Get Public Lists](actions/get-public-lists.md) | GET | Retrieves all public lists from Dotdigital. |

### Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get Preferences](actions/get-preferences.md) | GET | Retrieves preferences and preference categories from Dotdigital. |
| [Get Preferences for Contact](actions/get-preferences-for-contact.md) | GET | Retrieves a contact's preference opt-ins from Dotdigital. |

### Program

| Action | Method | Description |
| --- | --- | --- |
| [Get Program by ID](actions/get-program-by-id.md) | GET | Retrieves a program from Dotdigital by ID. |
| [Get Programs](actions/get-programs.md) | GET | Retrieves all account programs from Dotdigital. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Segments](actions/get-segments.md) | GET | Retrieves all saved segments from Dotdigital. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriptions for Contact](actions/get-subscriptions-for-contact.md) | GET | Retrieves subscriptions for a contact from Dotdigital. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new email campaign template in Dotdigital. |
| [Get Template by ID](actions/get-template-by-id.md) | GET | Retrieves an email campaign template from Dotdigital by ID. |
| [Get Templates](actions/get-templates.md) | GET | Retrieves email campaign templates from Dotdigital. |

