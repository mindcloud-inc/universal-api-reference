# Change Integration Setting with MailFloss

Updates an integration setting in MailFloss.

## Endpoint

- **Method:** `POST`
- **Path:** `/settings/:id`
- **Base URL:** `https://api.mailfloss.com`
- **Official documentation:** [Change Integration Setting](https://developers.mailfloss.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Integration setting ID. |
| `id` | path | `string` | yes | Integration ID to update. |
| `type` | body | `string` | yes | Setting type to modify. MailFloss documents whitelist, blacklist, aggressiveness, frequency, or action. |
| `data.keyword` | body | `string` | no | Keyword used for blacklist or whitelist insertion. |
| `data.processed` | body | `boolean` | no | Whether the job has finished processing. |
| `data.localpart` | body | `boolean` | no | Use the localpart for blacklist or whitelist insertion. |
| `data.domain` | body | `boolean` | no | Use the domain for blacklist or whitelist insertion. |
| `data.email` | body | `boolean` | no | Use the whole email address for blacklist or whitelist insertion. |
| `data.match` | body | `string` | no | Match type. MailFloss documents exact or contains. |
