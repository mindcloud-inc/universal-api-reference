# Add Session Ticket Types To Session with Mighty Tix

Adds session ticket types to a session in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Add Session Ticket Types To Session](https://mightytix.com/docs/admin-api#mutation-addSessionTicketTypesToSession)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | AddSessionTicketTypesToSessionInput object from the Mighty Tix Admin GraphQL docs. |
