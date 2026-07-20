# <img src="https://images.mindcloud.co/apps/icons/planning-center_1773258893572.png" alt="Planning Center logo" width="28" height="28"> Planning Center: Universal API

Organize ministries, coordinate events, plan services, and connect your congregation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/planningCenter/latest
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.planningcenter.com
- **Vendor API docs:** https://api.planningcenteronline.com/docs/apps

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List People](actions/list-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [List Person Addresses](actions/list-person-addresses.md) | GET | Retrieves addresses for a person in Planning Center. |

### Campus

| Action | Method | Description |
| --- | --- | --- |
| [List Campuses](actions/list-campuses.md) | GET | Retrieves campuses from Planning Center. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [List Person Emails](actions/list-person-emails.md) | GET | Retrieves email addresses for a person in Planning Center. |

### Fielddatum

| Action | Method | Description |
| --- | --- | --- |
| [List Person Field Data](actions/list-person-field-data.md) | GET | Retrieves field data for a person in Planning Center. |

### Household

| Action | Method | Description |
| --- | --- | --- |
| [Create Household](actions/create-household.md) | POST | Creates a new household in Planning Center. |
| [Get Household](actions/get-household.md) | GET | Retrieves a household from Planning Center. |
| [List Households](actions/list-households.md) | GET | Retrieves households from Planning Center. |
| [List Person Households](actions/list-person-households.md) | GET | Retrieves households for a person in Planning Center. |
| [Update Household](actions/update-household.md) | PUT | Updates an existing household in Planning Center. |

### Householdmembership

| Action | Method | Description |
| --- | --- | --- |
| [Create Household Membership](actions/create-household-membership.md) | POST | Creates a household membership in Planning Center. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Planning Center. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from Planning Center. |

### Listresult

| Action | Method | Description |
| --- | --- | --- |
| [List List Results](actions/list-list-results.md) | GET | Retrieves results for a list in Planning Center. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Person Notes](actions/list-person-notes.md) | GET | Retrieves notes for a person in Planning Center. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Planning Center. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Planning Center. |
| [List Household People](actions/list-household-people.md) | GET | Retrieves people in a household from Planning Center. |
| [List People](actions/list-people.md) | GET | Retrieves people from Planning Center. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Planning Center. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Person Phone Numbers](actions/list-person-phone-numbers.md) | GET | Retrieves phone numbers for a person in Planning Center. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from Planning Center. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from Planning Center. |

### Workflowcard

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Cards](actions/list-workflow-cards.md) | GET | Retrieves workflow cards for a person in Planning Center. |

