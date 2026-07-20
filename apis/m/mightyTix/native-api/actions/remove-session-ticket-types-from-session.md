# Remove Session Ticket Types From Session with Mighty Tix

Removes session ticket types from a session in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Remove Session Ticket Types From Session](https://mightytix.com/docs/admin-api#mutation-removeSessionTicketTypesFromSession)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | RemoveSessionTicketTypesFromSessionInput object from the Mighty Tix Admin GraphQL docs. |
