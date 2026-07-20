# Create Person with Cloze

Creates a person in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/create`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Create Person](https://api.cloze.com/api-docs/#/paths/v1-people-create/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dryrun` | body | `boolean` | no | Run validation without creating or updating the record |
| `emails[]` | body | `array<object>` | no | Array of email addresses |
| `emails[].preferred` | body | `boolean` | no | Make this the preferred email address |
| `emails[].type` | body | `list<string>` | no | Alternative to work or home fields when submitting records to Cloze Accepted values: `bulk`, `home`, `work`. |
| `emails[].value` | body | `string` | no | The email address |
| `emails[].work` | body | `boolean` | no | Whether this is a work address |
| `first` | body | `string` | no | First name of the person |
| `last` | body | `string` | no | Last name of the person |
| `name` | body | `string` | no | Full name of the person |
| `segment` | body | `string` | no | Segment of the person |
| `stage` | body | `list<string>` | no | Stage of the person Accepted values: `current`, `future`, `lead`, `out`, `past`. |
