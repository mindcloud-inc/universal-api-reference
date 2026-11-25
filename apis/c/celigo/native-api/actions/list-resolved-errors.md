# List Resolved Errors with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/flows/:flowId/:stepId/resolved`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [List Resolved Errors](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `list<string>` | yes | Flow that owns the step. |
| `stepId` | path | `string` | yes | Export or import ID of the flow step. Get it from Get Flow (pageGenerators / pageProcessors) or Get Flow Error Summary. |
| `resolvedAt_gte` | query | `date` | no | Only return errors resolved at or after this time. Required when Flow Job ID is set. |
| `resolvedAt_lte` | query | `date` | no | Only return errors resolved at or before this time. |
| `occurredAt_gte` | query | `date` | no | Only return errors that originally occurred at or after this time. |
| `occurredAt_lte` | query | `date` | no | Only return errors that originally occurred at or before this time. |
| `_flowJobId` | query | `string` | no | Only return errors from this flow-run job. Must be sent with Resolved at or After. |
| `tags[]` | query | `array<string>` | no | Only return errors carrying at least one of these tag IDs. |
| `resolvedBy[]` | query | `array<string>` | no | Only return errors resolved by these user IDs. |
