# Remove Contact From Campaign with Emelia

Deletes a contact from an Emelia campaign by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [Remove Contact From Campaign](https://docs-old.emelia.io/#operation-remove_contact_from_a_campaign-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email address |
| `id` | body | `string` | yes | Campaign identifier |
