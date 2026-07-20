# Update Profile with Raisely

Updates an existing profile in Raisely.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles/:path`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Update Profile](https://developers.raisely.com/reference/patchprofile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | query | `string` | no | The `uuid`, `path` or domain of the campaign to associate with the request |
| `partial` | query | `boolean` | no | Determines if a record updates public/private values in a merge verses an overwrite |
| `data` | body | `object` | no | — |
| `currency` | body | `string` | no | 3 letter currency code Examples: `AUD`, `USD` |
| `description` | body | `string` | no | Public description of the fundraiser profile Example: `I believe in a better world` |
| `exerciseGoal` | body | `number` | no | The exercise distance goal for the profile, in metres Example: `12345` |
| `exerciseGoalTime` | body | `number` | no | The time spent exercising goal for the profile, in minutes Example: `12345` |
| `fundraiserTheme` | body | `string` | no | Path of the DIY fundraiser theme selected by the fundraiser Examples: `birthday`, `bake-sale` |
| `goal` | body | `number` | no | Fundraising target (in cents) Example: `100050` |
| `name` | body | `string` | no | The name of the profile Example: `Bob D.` |
| `path` | path | `string` | no | The path of this record (for alternative lookup) Example: `bobd` |
| `photoUrl` | body | `string` | no | URL of the profile photo Example: `https://raisely-images.imgix.net/www/uploads/t-03-arl-8-es-uhhqua-4-pr-f-4865431-df-58-512-png-08e3f5.png` |
| `private` | query | `object` | no | Private values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `pronouns` | body | `string` | no | Pronouns of the profile |
| `public` | body | `object` | no | Public values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `type` | body | `string` | no | INDIVIDUAL, GROUP or ORGANISATION Examples: `INDIVIDUAL`, `GROUP`, `ORGANISATION` |
| `overwriteCustomFields` | body | `boolean` | no | If passed, replace the existing `public` and `private` values on the record with the values provided with this payload |
