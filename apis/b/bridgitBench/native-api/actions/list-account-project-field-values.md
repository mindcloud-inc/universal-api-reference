# List Account Project Field Values with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/Accounts/:id/project-field-values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Account Project Field Values](https://developers.gobridgit.com/reference/accounts_queryprojectfieldvalues)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Account ID |
| `includeEmpty` | query | `boolean` | no | If true, the response will include all project field values, even if no value is set for a given field. If false, field values that are empty are not included in the response. |
| `projectIds` | query | `number` | no | Optional paramater of comma delimited ids for filtering results based on the project IDs provided Send multiple values as a string separated by `,`. |
| `projectNumber` | query | `string` | no | Optional - for filtering result by system field "Project Number" |
| `externalId` | query | `string` | no | Optional - for filtering result by system field "External ID" |
| `classification` | query | `list<string>` | no | Optional - for filtering result by classification: All or Experience" Accepted values: `All`, `Experience`. |
