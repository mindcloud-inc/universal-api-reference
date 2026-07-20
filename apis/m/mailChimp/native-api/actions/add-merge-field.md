# Add Merge Field with Mailchimp

Creates a new merge field in a Mailchimp audience.

## Endpoint

- **Method:** `POST`
- **Path:** `lists/:list_id/merge-fields`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Add Merge Field](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/MergeFields/Collection.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `default_value` | body | `string` | no | — |
| `display_order` | body | `number` | no | — |
| `help_text` | body | `string` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `name` | body | `string` | yes | Merge field name. |
| `options` | body | `object` | no | — |
| `public` | body | `boolean` | no | — |
| `required` | body | `boolean` | no | — |
| `tag` | body | `string` | no | Merge field tag. |
| `type` | body | `list<string>` | yes | Merge field type. Accepted values: `address`, `birthday`, `date`, `dropdown`, `imageurl`, `number`, `phone`, `radio`, `text`, `url`, `zip`. |
