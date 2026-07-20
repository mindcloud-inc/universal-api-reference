# <img src="https://images.mindcloud.co/apps/icons/alpha-trans-form_1782739311699.png" alt="Alpha TransForm logo" width="28" height="28"> Alpha TransForm: Universal API

Manage TransForm forms, submissions, users, and workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/alphaTransForm/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://transform.alphasoftware.com
- **Vendor API docs:** https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/index.xml

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Status](actions/get-account-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Apikey

| Action | Method | Description |
| --- | --- | --- |
| [Get API Keys](actions/get-api-keys.md) | GET | Retrieves API keys from Alpha TransForm. |
| [Get API Scope Codes](actions/get-api-scope-codes.md) | GET | Retrieves API scope codes from Alpha TransForm. |

### Formdefinition

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Commands From Sample JSON](actions/create-form-commands-from-sample-json.md) | GET | Retrieves generated form commands from sample JSON in Alpha TransForm. |
| [Create Form Definition](actions/create-form-definition.md) | POST | Creates a new form definition in Alpha TransForm. |
| [Delete Form Definition](actions/delete-form-definition.md) | DELETE | Deletes an existing form definition from Alpha TransForm. |
| [Duplicate Form Definition](actions/duplicate-form-definition.md) | POST | Creates a duplicate form definition in Alpha TransForm. |
| [Get Fields In Form](actions/get-fields-in-form.md) | GET | Retrieves form fields from Alpha TransForm. |
| [Get Form Definition](actions/get-form-definition.md) | GET | Retrieves a form definition from Alpha TransForm. |
| [Get Form Definition Commands](actions/get-form-definition-commands.md) | GET | Retrieves form definition commands from Alpha TransForm. |
| [Get Form Media Field Names](actions/get-form-media-field-names.md) | GET | Retrieves form media field names from Alpha TransForm. |
| [List Form Definitions](actions/list-form-definitions.md) | GET | Retrieves form definitions from Alpha TransForm. |
| [Update Form Definition](actions/update-form-definition.md) | PUT | Updates an existing form definition in Alpha TransForm. |
| [Update Form Definition Commands](actions/update-form-definition-commands.md) | PUT | Updates form definition commands in Alpha TransForm. |

### Forminstance

| Action | Method | Description |
| --- | --- | --- |
| [Change Form Instance Data](actions/change-form-instance-data.md) | PUT | Updates data for a form instance in Alpha TransForm. |
| [Change Form Instance Metadata](actions/change-form-instance-metadata.md) | PUT | Updates form instance metadata in Alpha TransForm. |
| [Change Form Instance Status](actions/change-form-instance-status.md) | PUT | Updates a form instance status in Alpha TransForm. |
| [Create Form Instance](actions/create-form-instance.md) | POST | Creates a new form instance in Alpha TransForm. |
| [Delete Form Instance](actions/delete-form-instance.md) | DELETE | Deletes an existing form instance from Alpha TransForm. |
| [Execute On Submit Events](actions/execute-on-submit-events.md) | PUT | Executes on-submit events for a form instance in Alpha TransForm. |
| [Get Form Data Array For Form](actions/get-form-data-array-for-form.md) | GET | Retrieves form data for all instances of a form in Alpha TransForm. |
| [Get Form Data For Form Instance](actions/get-form-data-for-form-instance.md) | GET | Retrieves form data for a form instance in Alpha TransForm. |
| [List Form Instances Across All Forms](actions/list-form-instances-across-all-forms.md) | GET | Retrieves form instance data across all forms in Alpha TransForm. |
| [List Form Instances For Form](actions/list-form-instances-for-form.md) | GET | Retrieves form instance data for a form in Alpha TransForm. |
| [Render Form As HTML](actions/render-form-as-html.md) | GET | Retrieves rendered HTML for form data in Alpha TransForm. |

### Formlookup

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Lookup List](actions/get-form-lookup-list.md) | GET | Retrieves list field choices from Alpha TransForm. |
| [Set Form Lookup List](actions/set-form-lookup-list.md) | PUT | Updates list field choices in Alpha TransForm. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Integrations In Account](actions/list-integrations-in-account.md) | GET | Retrieves connected applications from Alpha TransForm. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Send Notification To User](actions/send-notification-to-user.md) | POST | Sends an email or SMS notification to a user in Alpha TransForm. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Roles In Account](actions/delete-user-roles-in-account.md) | DELETE | Deletes a user's account roles from Alpha TransForm. |
| [Get Roles In Account](actions/get-roles-in-account.md) | GET | Retrieves account roles from Alpha TransForm. |
| [Get User Roles In Account](actions/get-user-roles-in-account.md) | GET | Retrieves a user's account roles from Alpha TransForm. |
| [Set User Roles In Account](actions/set-user-roles-in-account.md) | PUT | Updates a user's account roles in Alpha TransForm. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Account](actions/add-user-to-account.md) | POST | Adds a user to an Alpha TransForm account. |
| [Change Form Instance User](actions/change-form-instance-user.md) | PUT | Updates the user for a form instance in Alpha TransForm. |
| [Change User Display Name](actions/change-user-display-name.md) | PUT | Updates a user's display name in Alpha TransForm. |
| [Create User Account](actions/create-user-account.md) | POST | Creates a new user account in Alpha TransForm. |
| [Invite Users](actions/invite-users.md) | POST | Invites users to create Alpha TransForm accounts. |
| [List Users In Account](actions/list-users-in-account.md) | GET | Retrieves account users from Alpha TransForm. |
| [Remove User From Account](actions/remove-user-from-account.md) | DELETE | Removes a user from an Alpha TransForm account. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Status](actions/get-account-status.md) | GET | Retrieves account status from Alpha TransForm. |

