# Update a single sdk connection with GrowthBook

Updates an existing SDK connection in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sdk-connections/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single sdk connection](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `name` | body | `string` | no | — |
| `language` | body | `string` | no | — |
| `sdkVersion` | body | `string` | no | — |
| `environment` | body | `string` | no | — |
| `projects` | body | `list<string>` | no | — |
| `encryptPayload` | body | `boolean` | no | — |
| `includeVisualExperiments` | body | `boolean` | no | — |
| `includeDraftExperiments` | body | `boolean` | no | — |
| `includeExperimentNames` | body | `boolean` | no | — |
| `includeRedirectExperiments` | body | `boolean` | no | — |
| `includeRuleIds` | body | `boolean` | no | — |
| `includeProjectIdInMetadata` | body | `boolean` | no | — |
| `includeCustomFieldsInMetadata` | body | `boolean` | no | — |
| `allowedCustomFieldsInMetadata` | body | `list<string>` | no | — |
| `includeTagsInMetadata` | body | `boolean` | no | — |
| `proxyEnabled` | body | `boolean` | no | — |
| `proxyHost` | body | `string` | no | — |
| `hashSecureAttributes` | body | `boolean` | no | — |
| `remoteEvalEnabled` | body | `boolean` | no | — |
| `savedGroupReferencesEnabled` | body | `boolean` | no | — |
