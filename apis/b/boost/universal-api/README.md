# <img src="https://images.mindcloud.co/apps/icons/boost_1777641599958.png" alt="Boost logo" width="28" height="28"> Boost: Universal API

Boost.space centralizes company data, CRM, business operations, documents, tasks, and automation resources behind a workspace-specific REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/boost/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://boost.space
- **Vendor API docs:** https://apidoc.boost.space/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Activity](actions/get-activity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-activity?connectionId=$CONNECTION_ID&activityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity type from Boost by ID. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activity types available in Boost. |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Address](actions/get-address.md) | GET | Retrieves an address from Boost by ID. |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves address records available in Boost. |

### Appflow

| Action | Method | Description |
| --- | --- | --- |
| [Get AppFlow](actions/get-appflow.md) | GET | Retrieves an appflow from Boost by ID. |
| [List AppFlows](actions/list-appflows.md) | GET | Retrieves appflow records available in Boost. |

### Automation Action

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation Action](actions/get-automation-action.md) | GET | Retrieves an automation action from Boost by ID. |
| [List Automation Actions](actions/list-automation-actions.md) | GET | Retrieves automation action records from Boost. |

### Automation Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation Trigger](actions/get-automation-trigger.md) | GET | Retrieves an automation trigger from Boost by ID. |
| [List Automation Triggers](actions/list-automation-triggers.md) | GET | Retrieves automation trigger records from Boost. |

### Business Case

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Case](actions/get-business-case.md) | GET | Retrieves a business case from Boost by ID. |
| [List Business Cases](actions/list-business-cases.md) | GET | Retrieves business case records from Boost. |

### Business Contract

| Action | Method | Description |
| --- | --- | --- |
| [List Business Contracts](actions/list-business-contracts.md) | GET | Retrieves business contract records from Boost. |

### Business Offer

| Action | Method | Description |
| --- | --- | --- |
| [List Business Offers](actions/list-business-offers.md) | GET | Retrieves business offer records from Boost. |

### Business Order

| Action | Method | Description |
| --- | --- | --- |
| [List Business Orders](actions/list-business-orders.md) | GET | Retrieves business order records from Boost. |

### Chart

| Action | Method | Description |
| --- | --- | --- |
| [List Charts](actions/list-charts.md) | GET | Retrieves chart records available in Boost. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Boost by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records available in Boost. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom field records from Boost. |

### Custom Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Module](actions/get-custom-module.md) | GET | Retrieves a custom module from Boost by ID. |
| [List Custom Modules](actions/list-custom-modules.md) | GET | Retrieves custom module records from Boost. |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboard records available in Boost. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a file record from Boost by ID. |
| [List Files](actions/list-files.md) | GET | Retrieves file records available in Boost. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Boost by ID. |
| [List Forms](actions/list-forms.md) | GET | Retrieves form records available in Boost. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Get Space](actions/get-space.md) | GET | Retrieves a space from Boost by ID. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves workspace records available in Boost. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Boost by ID. |
| [List Users](actions/list-users.md) | GET | Finds users in Boost by search criteria. |

