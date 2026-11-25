# List Open Errors with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/flows/:flowId/:stepId/errors`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [List Open Errors](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `list<string>` | yes | Flow that owns the step. |
| `stepId` | path | `string` | yes | Export or import ID of the flow step. Get it from Get Flow (pageGenerators / pageProcessors) or Get Flow Error Summary. |
| `occurredAt_gte` | query | `date` | no | Only return errors that occurred at or after this time. Required when Flow Job ID is set. |
| `occurredAt_lte` | query | `date` | no | Only return errors that occurred at or before this time. |
| `_flowJobId` | query | `string` | no | Only return errors from this flow-run job. Must be sent with Occurred at or After. |
| `tags[]` | query | `array<string>` | no | Only return errors carrying at least one of these tag IDs. |
