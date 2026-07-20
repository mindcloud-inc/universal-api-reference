# Create Project with Cinode

Creates a new project in Cinode.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0.1/companies/:companyId/projects`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Create Project](https://api.cinode.com/docs/index.html#/Project/NewCompanyProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company ID. |
| `title` | body | `string` | yes | Project title. |
| `customerId` | body | `number` | yes | Customer ID linked to the project. |
| `description` | body | `string` | no | Project description. |
| `internalId` | body | `string` | no | Internal project identifier. |
| `externalId` | body | `string` | no | External project identifier. |
| `estimatedCloseDate` | body | `date` | no | Estimated close date. |
| `estimatedValue` | body | `number` | no | Estimated project value. |
| `contractValue` | body | `number` | no | Contract value. |
| `probability` | body | `number` | no | Project probability. |
| `projectState` | body | `number` | no | Project state enum. 0=Open, 30=Won, 40=Lost, 50=Abandoned, 60=Suspended. |
