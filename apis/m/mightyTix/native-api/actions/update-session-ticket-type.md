# Update Session Ticket Type with Mighty Tix

Updates an existing session ticket type in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Update Session Ticket Type](https://mightytix.com/docs/admin-api#mutation-updateOneSessionTicketType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | UpdateOneSessionTicketTypeInput object from the Mighty Tix Admin GraphQL docs. |
