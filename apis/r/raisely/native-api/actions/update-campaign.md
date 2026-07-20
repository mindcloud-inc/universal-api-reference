# Update Campaign with Raisely

Updates an existing campaign in Raisely.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns/:campaign`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Update Campaign](https://developers.raisely.com/reference/patchcampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | path | `string` | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `data` | body | `object` | no | — |
| `allowExperiments` | body | `boolean` | no | Allows the campaign to participate in Raisely experiments Examples: `true`, `false` |
| `currency` | body | `string` | no | 3 letter currency code Examples: `AUD`, `USD` |
| `defaultCampaignFund` | body | `string` | no | Fund that is assigned as the default fund for the campaign |
| `goal` | body | `number` | no | (in cents) Example: `500050` |
| `mode` | body | `string` | no | Mode for payment processing. Make sure to set this to LIVE before launching your campaign so you can take real donations. Examples: `LIVE`, `TEST` |
| `name` | body | `string` | no | Name of the campaign Example: `<< campaign name >>` |
| `path` | body | `string` | no | The path of this record (for alternative lookup) Example: `run-for-a-cure` |
| `primaryDomain` | body | `string` | no | Primary domain of the campaign |
| `private` | query | `object` | no | Private values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `public` | body | `object` | no | Public values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `publicKey` | body | `string` | no | (Internal Raisely field - ignored) Example: `aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaaa` |
| `theme` | body | `string` | no | The theme name by this campaign Examples: `donation-basic`, `donation-modern`, `donation-elegant`, `donation-expansive`, `donation-impact`, `donation-elegant`, `donation-active`, `peerToPeer-basic`, `peerToPeer-modern`, `peerToPeer-elegant`, `peerToPeer-expansive`, `peerToPeer-impact`, `peerToPeer-elegant`, `peerToPeer-active`, `appealsHub-basic`, `appealsHub-modern`, `appealsHub-elegant`, `appealsHub-expansive`, `appealsHub-impact`, `appealsHub-elegant`, `appealsHub-active`, `communityHub-basic`, `communityHub-modern`, `communityHub-elegant`, `communityHub-expansive`, `communityHub-impact`, `communityHub-elegant`, `communityHub-active`, `appeal-basic`, `appeal-modern`, `appeal-elegant`, `appeal-expansive`, `appeal-impact`, `appeal-elegant`, `appeal-active`, `special-virtualEvent`, `special-virtualAppeal`, `special-charityChallenge` |
| `urls[]` | body | `array<string>` | no | Custom domains of the campaign Example: `[   "yourdomain.com" ]` |
| `urls[]` | body | `array<string>` | no | Custom domains of the campaign Example: `[   "yourdomain.com" ]` |
| `version` | body | `string` | no | Theme version Example: `3.0.0` |
| `overwriteCustomFields` | body | `boolean` | no | If passed, replace the existing `public` and `private` values on the record with the values provided with this payload |
