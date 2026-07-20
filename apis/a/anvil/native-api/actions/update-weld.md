# Update Weld with Anvil

Updates an existing weld in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Weld](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateWeld)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Update Weld. |
| `variables.name` | body | `string` | no | Provide Name for Update Weld. |
| `variables.slug` | body | `string` | no | Provide Slug for Update Weld. |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Update Weld. |
| `variables.visibility` | body | `string` | no | Provide Visibility for Update Weld. |
| `variables.config` | body | `object` | no | Provide Config for Update Weld. |
| `variables.configFile` | body | `file` | no | Provide Config File for Update Weld. |
| `variables.isArchived` | body | `boolean` | no | Provide Is Archived for Update Weld. |
| `variables.expiresAt` | body | `string` | no | Provide Expires At for Update Weld. |
| `variables.draftStep` | body | `string` | no | Provide Draft Step for Update Weld. |
| `variables.entryForgeId` | body | `number` | no | Provide Entry Forge ID for Update Weld. |
| `variables.entryButtonText` | body | `string` | no | Provide Entry Button Text for Update Weld. |
| `variables.entryButtonCopyLink` | body | `boolean` | no | Provide Entry Button Copy Link for Update Weld. |
| `variables.signatureEmailSubject` | body | `object` | no | Provide Signature Email Subject for Update Weld. |
| `variables.signatureEmailBody` | body | `object` | no | Provide Signature Email Body for Update Weld. |
| `variables.dataDisplayTitle` | body | `object` | no | Provide Data Display Title for Update Weld. |
| `variables.signatureMode` | body | `string` | no | Provide Signature Mode for Update Weld. |
| `variables.signatureProvider` | body | `string` | no | Provide Signature Provider for Update Weld. |
| `variables.lockedTitleNew` | body | `string` | no | Provide Locked Title New for Update Weld. |
| `variables.lockedDescriptionNew` | body | `string` | no | Provide Locked Description New for Update Weld. |
| `variables.lockedTitleExisting` | body | `string` | no | Provide Locked Title Existing for Update Weld. |
| `variables.lockedDescriptionExisting` | body | `string` | no | Provide Locked Description Existing for Update Weld. |
| `variables.expireAfterDaysComplete` | body | `number` | no | Provide Expire After Days Complete for Update Weld. |
| `variables.expireAfterDaysStart` | body | `number` | no | Provide Expire After Days Start for Update Weld. |
| `variables.planEid` | body | `string` | no | Provide Plan EID for Update Weld. |
| `variables.steps` | body | `object` | no | Provide Steps for Update Weld. |
| `variables.signatureStepsMode` | body | `string` | no | Provide Signature Steps Mode for Update Weld. |
| `variables.versionNumber` | body | `number` | no | Provide Version Number for Update Weld. |
| `variables.weldCompleteEmailRecipients` | body | `object` | no | Provide Weld Complete Email Recipients for Update Weld. |
| `variables.weldCompleteEmailEnableForTest` | body | `boolean` | no | Provide Weld Complete Email Enable For Test for Update Weld. |
| `variables.mergePDFs` | body | `boolean` | no | Provide Merge PDFs for Update Weld. |
