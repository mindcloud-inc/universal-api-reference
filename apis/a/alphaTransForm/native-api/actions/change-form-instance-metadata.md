# Change Form Instance Metadata with Alpha TransForm

Updates form instance metadata in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/ChangeFormInstanceMetaData/:formInstanceId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Change Form Instance Metadata](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeFormInstanceMetaData.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formInstanceId` | path | `string` | yes | formInstanceId of the form instance whose meta data should be changed |
| `status` | body | `string` | no | updated form status - if blank, then the status is not changed |
| `person` | body | `string` | no | person to whom form is assigned - if blank, the person is not changed. If ^blank^, person is set to blank |
| `duedate` | body | `string` | no | due date for the form. Use yyyy-MM-dd format. If ^blank^, set to blank. |
| `user1` | body | `string` | no | User field |
| `user2` | body | `string` | no | User field |
| `user3` | body | `string` | no | User field |
| `user4` | body | `string` | no | User field |
| `user5` | body | `string` | no | User field |
| `userlabel1` | body | `string` | no | User field |
| `userlabel2` | body | `string` | no | User field |
| `userlabel3` | body | `string` | no | User field |
| `userlabel4` | body | `string` | no | User field |
| `userlabel5` | body | `string` | no | User field |
