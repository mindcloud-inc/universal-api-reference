# List Emails with Boomlify

Retrieves active temporary emails from Boomlify.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/emails`
- **Base URL:** `https://v1.boomlify.com`
- **Official documentation:** [List Emails](https://boomlify.com/en/temp-mail-api-docs?endpoint=list-emails&tab=docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_expired` | query | `boolean` | no | Whether expired emails should be included. |
| `permanent_only` | query | `boolean` | no | Whether to return only permanent emails. |
| `include_permanent` | query | `boolean` | no | Whether permanent emails should be included. |
