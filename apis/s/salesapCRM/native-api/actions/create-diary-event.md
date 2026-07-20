# Create Diary Event with SalesapCRM

Creates a diary event in SalesapCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/diary-events`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Create Diary Event](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API data object for a diary event, including type, attributes, and optional relationships. |
