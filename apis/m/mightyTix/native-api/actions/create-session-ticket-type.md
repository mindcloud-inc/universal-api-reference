# Create Session Ticket Type with Mighty Tix

Creates a new session ticket type in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Create Session Ticket Type](https://mightytix.com/docs/admin-api#mutation-createOneSessionTicketType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | CreateOneSessionTicketTypeInput object from the Mighty Tix Admin GraphQL docs. |
