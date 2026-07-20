# List Filtered Addresses with Starshipit

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbook/filtered`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [List Filtered Addresses](https://api-docs.starshipit.com/#4f93a04a-c4db-40bf-86d5-f4f8fd3fb265)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Which page of the address book to return |
| `page_size` | query | `number` | no | Number of records per page |
| `sort` | query | `string` | no | Sort by column. Available values: None, Name, Company, Street, Suburb, PostCode, City, State, Country, Code, Phone, Email |
| `sort_direction` | query | `string` | no | Sort direction for the sort column. Available values: None, Ascending, Descending |
