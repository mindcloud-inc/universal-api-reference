# Update Ticket Type with Mighty Tix

Updates an existing ticket type in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Update Ticket Type](https://mightytix.com/docs/admin-api#mutation-updateOneTicketType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | UpdateOneTicketTypeInput object from the Mighty Tix Admin GraphQL docs. |
