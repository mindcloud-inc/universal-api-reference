# List People with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List People](https://developers.gobridgit.com/reference/persons_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `email` | query | `string` | no | Filter user with email |
| `state` | query | `list<string>` | no | If specified and not 'Unknown', only include people matching the given state. The available values are defined as follows: - Unknown: By default, includes only Active people. - Active: include only Active people - Deactivated: include only Deactivated people - All: include all people, regardless of state Accepted values: `Active`, `All`, `Deactivated`. |
| `ids` | query | `number` | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Send multiple values as a string separated by `,`. |
| `uniqueId` | query | `string` | no | Optional paramater of unique identifier for filtering results based on the person unique identifier provided |
