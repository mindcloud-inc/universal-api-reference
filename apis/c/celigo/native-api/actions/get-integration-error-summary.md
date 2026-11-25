# Get Integration Error Summary with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/integrations/:integrationId/errors`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [Get Integration Error Summary](https://developer.celigo.com/api/api-reference/integrations-and-flows/integrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integrationId` | path | `list<string>` | yes | Integration to summarize open errors for. |
