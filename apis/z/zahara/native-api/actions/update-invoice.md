# Update Invoice with Zahara

Updates an existing invoice in Zahara.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/{businessUnitApiKey}/Invoice/Update/{{documentId}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Update Invoice](https://ask.zaharasoftware.com/api-docs/update-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | Invoice document ID to update. |
