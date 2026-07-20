# Create Ticket Type with Mighty Tix

Creates a new ticket type in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Create Ticket Type](https://mightytix.com/docs/admin-api#mutation-createOneTicketType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | CreateOneTicketTypeInput object from the Mighty Tix Admin GraphQL docs. |
