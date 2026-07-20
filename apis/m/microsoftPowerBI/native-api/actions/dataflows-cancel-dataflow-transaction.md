# Cancel Dataflow Transaction with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/dataflows/transactions/[:transactionId]/cancel`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Cancel Dataflow Transaction](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/cancel-dataflow-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `transactionId` | path | `string` | yes | The transaction ID |
