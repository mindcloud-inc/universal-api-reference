# <img src="https://images.mindcloud.co/apps/icons/coast_1782918415997.png" alt="Coast logo" width="28" height="28"> Coast: Universal API

Use the Coast API to manage account settings, cards, departments, locations, people, policies, roles, purchases, and vehicles within a Coast account.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coast/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://coastpay.com
- **Vendor API docs:** https://coastpay.com/integrations/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Account](actions/getmyaccount.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getmyaccount?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get My Account](actions/getmyaccount.md) | GET |  |

### Account Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update My Account Settings](actions/updatemyaccountsettings.md) | PUT |  |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Get Card By ID](actions/getcard.md) | GET |  |
| [Get All Cards](actions/getcards.md) | GET |  |
| [Update Everyday Purchase Card By ID](actions/updateeverydaypurchasecardbyid.md) | PUT |  |
| [Update Fleet Card By ID](actions/updatefleetcardbyid.md) | PUT |  |
| [Update Personalized Card By ID](actions/updatepersonalizedcardbyid.md) | PUT |  |
| [Update Project Card By ID](actions/updateprojectcardbyid.md) | PUT |  |
| [Update Subscription Card By ID](actions/updatesubscriptioncardbyid.md) | PUT |  |
| [Update Vehicle PIN Card By ID](actions/updatevehiclepincardbyid.md) | PUT |  |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [Create Department](actions/createdepartment.md) | POST |  |
| [Delete Department By ID](actions/deletedepartment.md) | DELETE |  |
| [Get Department By ID](actions/getdepartment.md) | GET |  |
| [Get All Departments](actions/getdepartments.md) | GET |  |
| [Update Department By ID](actions/updatedepartment.md) | PUT |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/createlocation.md) | POST |  |
| [Delete Location By ID](actions/deletelocation.md) | DELETE |  |
| [Get Location By ID](actions/getlocation.md) | GET |  |
| [Get All Locations](actions/getlocations.md) | GET |  |
| [Update Location By ID](actions/updatelocation.md) | PUT |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/createperson.md) | POST |  |
| [Get All People](actions/getpeople.md) | GET |  |
| [Get Person By ID](actions/getperson.md) | GET |  |
| [Update Person By ID](actions/updateperson.md) | PUT |  |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [Create Policy](actions/createpolicy.md) | POST |  |
| [Get All Policies](actions/getpolicies.md) | GET |  |
| [Get Policy By ID](actions/getpolicy.md) | GET |  |
| [Update Policy By ID](actions/updatepolicy.md) | PUT |  |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase By ID](actions/getpurchase.md) | GET |  |
| [Get All Purchases](actions/getpurchases.md) | GET |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/createrole.md) | POST |  |
| [Get Role By ID](actions/getrole.md) | GET |  |
| [Get All Roles](actions/getroles.md) | GET |  |
| [Update Role By ID](actions/updaterole.md) | PUT |  |

### Telematic

| Action | Method | Description |
| --- | --- | --- |
| [Update Vehicle Stats](actions/updatevehiclestats.md) | POST |  |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Create Vehicle](actions/createvehicle.md) | POST |  |
| [Get Vehicle By ID](actions/getvehicle.md) | GET |  |
| [Get All Vehicles](actions/getvehicles.md) | GET |  |
| [Update Vehicle By ID](actions/updatevehicle.md) | PUT |  |

### Virtual Card

| Action | Method | Description |
| --- | --- | --- |
| [Order Everyday Purchase Virtual Card](actions/ordereverydaypurchasevirtualcard.md) | POST |  |
| [Order Project Virtual Card](actions/orderprojectvirtualcard.md) | POST |  |
| [Order Subscription Virtual Card](actions/ordersubscriptionvirtualcard.md) | POST |  |

