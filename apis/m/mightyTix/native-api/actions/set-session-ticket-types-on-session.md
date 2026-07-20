# Set Session Ticket Types On Session with Mighty Tix

Sets session ticket types on a session in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Set Session Ticket Types On Session](https://mightytix.com/docs/admin-api#mutation-setSessionTicketTypesOnSession)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | SetSessionTicketTypesOnSessionInput object from the Mighty Tix Admin GraphQL docs. |
