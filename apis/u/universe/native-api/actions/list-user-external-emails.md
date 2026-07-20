# List User External Emails with Universe

Retrieves external email addresses for a Universe user.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [List User External Emails](https://developers.universe.com/docs/basic-usage-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query document to execute for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables object for this query. |
