# List Subscription Pushes with Woztell

Retrieves subscription pushes from your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [List Subscription Pushes](https://doc.woztell.com/open-api-reference/#query-apiViewer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include first, after, before, subscriptionPushIds, search, and sortBy. |
