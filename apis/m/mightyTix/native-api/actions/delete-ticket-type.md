# Delete Ticket Type with Mighty Tix

Deletes an existing ticket type from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Delete Ticket Type](https://mightytix.com/docs/admin-api#mutation-deleteOneTicketType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | DeleteOneTicketTypeInput object from the Mighty Tix Admin GraphQL docs. |
