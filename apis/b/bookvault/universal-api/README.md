# <img src="https://images.mindcloud.co/apps/icons/group-15771_1780950979520.png" alt="Bookvault logo" width="28" height="28"> Bookvault: Universal API

Manage titles, orders, fulfillment, and shipping with Bookvault

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bookvault/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bookvault.app/
- **Vendor API docs:** https://api.bookvault.app/v3/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your account details from Bookvault. |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | POST | Creates a new address in Bookvault. |
| [Delete Address](actions/delete-address.md) | DELETE | Deletes an existing address from Bookvault. |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves saved addresses from your Bookvault account. |
| [Update Address](actions/update-address.md) | PUT | Updates an existing address in Bookvault. |

### Address Group

| Action | Method | Description |
| --- | --- | --- |
| [List Address Groups](actions/list-address-groups.md) | GET | Retrieves address groups from your Bookvault account. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [List Connected Apps](actions/list-connected-apps.md) | GET | Retrieves connected apps from your Bookvault account. |

### Binding

| Action | Method | Description |
| --- | --- | --- |
| [List Bindings](actions/list-bindings.md) | GET | Retrieves available bindings from Bookvault. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET | Retrieves available collections from Bookvault. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves available countries from Bookvault. |

### Ecologi Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Ecologi Statistics](actions/get-ecologi-statistics.md) | GET | Retrieves current Ecologi statistics from Bookvault. |

### Imprint

| Action | Method | Description |
| --- | --- | --- |
| [List Imprints](actions/list-imprints.md) | GET | Retrieves imprints from your Bookvault account. |

### Ioss Code

| Action | Method | Description |
| --- | --- | --- |
| [List IOSS Codes](actions/list-ioss-codes.md) | GET | Retrieves IOSS codes from your Bookvault account. |

### Promo Code

| Action | Method | Description |
| --- | --- | --- |
| [List Promo Codes](actions/list-promo-codes.md) | GET | Retrieves promotional codes from Bookvault. |

### Publisher

| Action | Method | Description |
| --- | --- | --- |
| [List Publishers](actions/list-publishers.md) | GET | Retrieves publishers from your Bookvault account. |

### Reporting Type

| Action | Method | Description |
| --- | --- | --- |
| [List Reporting Types](actions/list-reporting-types.md) | GET | Retrieves available reporting types from Bookvault. |

### Retailer

| Action | Method | Description |
| --- | --- | --- |
| [List Retailers](actions/list-retailers.md) | GET | Retrieves available retailers from Bookvault. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves active roles from your Bookvault account. |

### Size

| Action | Method | Description |
| --- | --- | --- |
| [List Sizes](actions/list-sizes.md) | GET | Retrieves available book sizes from Bookvault. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from your Bookvault account. |

