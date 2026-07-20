# Alpha TransForm: Native API Reference

A consolidated summary of Alpha TransForm's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/index.xml
- **API base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`

## Authentication

### API Key

Use a TransForm API key generated in TransForm Central.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://documentation.alphasoftware.com/TransFormDocumentation/pages/How%20To/create%20api%20key.xml)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User To Account](actions/add-user-to-account.md) | `GET /addUserToTransFormAccount/` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/AddUserToTransFormAccount.xml) |
| [Change Form Instance Data](actions/change-form-instance-data.md) | `POST /ChangeFormInstanceData/:formInstanceId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeFormInstanceData.xml) |
| [Change Form Instance Metadata](actions/change-form-instance-metadata.md) | `POST /ChangeFormInstanceMetaData/:formInstanceId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeFormInstanceMetaData.xml) |
| [Change Form Instance Status](actions/change-form-instance-status.md) | `GET /ChangeFormInstanceStatus` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeFormInstanceStatus.xml) |
| [Change Form Instance User](actions/change-form-instance-user.md) | `POST /ChangeFormInstanceUserId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeFormInstanceUserId.xml) |
| [Change User Display Name](actions/change-user-display-name.md) | `GET /changeUserDisplayName/:userId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeUserDisplayName.xml) |
| [Create Form Commands From Sample JSON](actions/create-form-commands-from-sample-json.md) | `POST /CreateFormCommandsFromSampleJSON` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/CreateFormCommandsFromSampleJSON.xml) |
| [Create Form Definition](actions/create-form-definition.md) | `POST /CreateNewFormDefinition` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/CreateNewFormDefinition.xml) |
| [Create Form Instance](actions/create-form-instance.md) | `POST /CreateNewFormInstance` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/CreateNewFormInstance.xml) |
| [Create User Account](actions/create-user-account.md) | `POST /createNewUserAccount` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/CreateNewUserAccount.xml) |
| [Delete Form Definition](actions/delete-form-definition.md) | `GET /DeleteFormDefinition/:formId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/DeleteFormDefinition.xml) |
| [Delete Form Instance](actions/delete-form-instance.md) | `GET /DeleteFormInstance/:formInstanceId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/DeleteFormInstance.xml) |
| [Delete User Roles In Account](actions/delete-user-roles-in-account.md) | `GET /deleteUserRolesInAccount/:userIdToDelete` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/DeleteUserRolesInAccount.xml) |
| [Duplicate Form Definition](actions/duplicate-form-definition.md) | `GET /DuplicateFormDefinition` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/DuplicateFormDefinition.xml) |
| [Execute On Submit Events](actions/execute-on-submit-events.md) | `POST /ExecuteOnSubmitEvents` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ExecuteOnSubmitEvents.xml) |
| [Get Account Status](actions/get-account-status.md) | `GET /GetAccountStatus` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetAccountStatus.xml) |
| [Get API Keys](actions/get-api-keys.md) | `GET /GetAPIKeys` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetAPIKeys.xml) |
| [Get API Scope Codes](actions/get-api-scope-codes.md) | `GET /getAPIScopeCodes` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetAPIScopeCodes.xml) |
| [Get Fields In Form](actions/get-fields-in-form.md) | `GET /GetFieldsInForm/:formId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFieldsInForm.xml) |
| [Get Form Data Array For Form](actions/get-form-data-array-for-form.md) | `GET /GetFormDataArrayForFormId/:formId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormDataArrayForFormId.xml) |
| [Get Form Data For Form Instance](actions/get-form-data-for-form-instance.md) | `GET /GetFormDataForFormInstanceId/:formInstanceId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormDataForFormInstanceId.xml) |
| [Get Form Definition](actions/get-form-definition.md) | `GET /GetFormDefinitionForFormId/:formId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormDefinitionForFormId.xml) |
| [Get Form Definition Commands](actions/get-form-definition-commands.md) | `GET /GetFormDefinitionCommandsForFormId/:formId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormDefinitionCommandsForFormId.xml) |
| [Get Form Lookup List](actions/get-form-lookup-list.md) | `GET /GetFormLookupList` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormLookupList.xml) |
| [Get Form Media Field Names](actions/get-form-media-field-names.md) | `GET /GetFormMediaFieldNamesForFormId/:formId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormMediaFieldNamesForFormId.xml) |
| [Get Roles In Account](actions/get-roles-in-account.md) | `GET /GetRolesInAccount` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetRolesInAccount.xml) |
| [Get User Roles In Account](actions/get-user-roles-in-account.md) | `GET /GetUserRolesInAccount/:userId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetUserRolesInAccount.xml) |
| [Invite Users](actions/invite-users.md) | `POST /inviteUsers/{accountId}` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/InviteUsers.xml) |
| [List Form Definitions](actions/list-form-definitions.md) | `GET /GetListOfFormDefinitionsForAccount` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetListOfFormDefinitionsForAccount.xml) |
| [List Form Instances Across All Forms](actions/list-form-instances-across-all-forms.md) | `GET /GetFormInstancesArrayForAllForms` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormInstancesArrayForAllForms.xml) |
| [List Form Instances For Form](actions/list-form-instances-for-form.md) | `GET /GetFormInstancesArrayForFormId/:formId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormInstancesArrayForFormId.xml) |
| [List Integrations In Account](actions/list-integrations-in-account.md) | `GET /GetListOfIntegrationsForAccount` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetListOfIntegrationsForAccount.xml) |
| [List Users In Account](actions/list-users-in-account.md) | `GET /getUsersInTransformAccount` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetUsersInTransformAccount.xml) |
| [Remove User From Account](actions/remove-user-from-account.md) | `POST /removeUserFromTransFormAccount/:accountToRemoveFrom` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/RemoveUserFromTransFormAccount.xml) |
| [Render Form As HTML](actions/render-form-as-html.md) | `POST /RenderFormAsHTML` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/RenderFormAsHTML.xml) |
| [Send Notification To User](actions/send-notification-to-user.md) | `POST /SendNotificationToUser` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/SendNotificationToUser.xml) |
| [Set Form Lookup List](actions/set-form-lookup-list.md) | `POST /SetFormLookupList/:formId/:fieldName` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/SetFormLookupList.xml) |
| [Set User Roles In Account](actions/set-user-roles-in-account.md) | `POST /setUserRolesInAccount/:userId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/SetUserRolesInAccount.xml) |
| [Update Form Definition](actions/update-form-definition.md) | `POST /UpdateFormDefinitionForFormId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/UpdateFormDefinitionForFormId.xml) |
| [Update Form Definition Commands](actions/update-form-definition-commands.md) | `POST /UpdateFormDefinitionCommandsForFormId/:formId` | [docs](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/UpdateFormDefinitionCommandsForFormId.xml) |
