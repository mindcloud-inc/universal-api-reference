# Unsubscribe Contact From List with Emailchef

Unsubscribes a contact from an Emailchef list.

## Endpoint

- **Method:** `POST`
- **Path:** `lists/:list_id/unsubscribe`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Unsubscribe Contact From List](https://emailchef.com/integration/#/Lists/unsubscribeContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The Emailchef list ID. |
| `contact_id` | query | `string` | yes | — |
