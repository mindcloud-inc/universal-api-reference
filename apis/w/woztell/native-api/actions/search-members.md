# Search Members with Woztell

Finds members in your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [Search Members](https://doc.woztell.com/open-api-reference/#query-apiViewer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include appId, first, after, before, channelId, externalIds, memberIds, firstName, lastName, gender, localeOperator, locales, and tagFilters. |
