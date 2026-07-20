# Update Organization with Anvil

Updates an existing organization in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Organization](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateOrganization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Update Organization. |
| `variables.organizationSlug` | body | `string` | no | Provide Organization Slug for Update Organization. |
| `variables.name` | body | `string` | no | Provide Name for Update Organization. |
| `variables.logo` | body | `file` | no | Provide Logo for Update Organization. |
| `variables.billingEmail` | body | `string` | no | Provide Billing Email for Update Organization. |
| `variables.supportEmail` | body | `string` | no | Provide Support Email for Update Organization. |
| `variables.slug` | body | `string` | no | Provide Slug for Update Organization. |
| `variables.defaultSourceId` | body | `string` | no | Provide Default Source ID for Update Organization. |
| `variables.signatureProvider` | body | `string` | no | Provide Signature Provider for Update Organization. |
| `variables.config` | body | `object` | no | Provide Config for Update Organization. |
| `variables.weldCompleteEmailRecipients` | body | `object` | no | Provide Weld Complete Email Recipients for Update Organization. |
| `variables.signerViewEmailRecipients` | body | `object` | no | Provide Signer View Email Recipients for Update Organization. |
| `variables.signerCompleteEmailRecipients` | body | `object` | no | Provide Signer Complete Email Recipients for Update Organization. |
| `variables.etchCompleteEmailRecipients` | body | `object` | no | Provide Etch Complete Email Recipients for Update Organization. |
| `variables.weldCompleteEmailEnableForTest` | body | `boolean` | no | Provide Weld Complete Email Enable For Test for Update Organization. |
| `variables.stylesheetURL` | body | `string` | no | Provide Stylesheet URL for Update Organization. |
| `variables.signerOptions` | body | `object` | no | Provide Signer Options for Update Organization. |
