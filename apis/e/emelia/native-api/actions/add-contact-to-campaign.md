# Add Contact To Campaign with Emelia

Adds a contact to a campaign in Emelia.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [Add Contact To Campaign](https://docs-old.emelia.io/#operation-add_contact_to_a_campaign-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `string` | yes | Contact payload JSON. Provide a JSON object string. |
| `id` | body | `string` | yes | Campaign identifier |
