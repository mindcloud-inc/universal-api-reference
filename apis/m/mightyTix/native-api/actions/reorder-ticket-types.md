# Reorder Ticket Types with Mighty Tix

Reorders ticket types in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Reorder Ticket Types](https://mightytix.com/docs/admin-api#mutation-reorderTicketTypes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | ReorderInput object from the Mighty Tix Admin GraphQL docs. |
