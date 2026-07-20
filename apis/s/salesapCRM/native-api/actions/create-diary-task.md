# Create Diary Task with SalesapCRM

Creates a diary task in SalesapCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/diary-tasks`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Create Diary Task](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API data object for a diary task, including type, attributes, and optional relationships. |
