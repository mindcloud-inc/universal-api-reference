# Create a single sdk connection with GrowthBook

Creates a new SDK connection in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk-connections`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single sdk connection](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `language` | body | `string` | yes |
| `sdkVersion` | body | `string` | no |
| `environment` | body | `string` | yes |
| `projects` | body | `list<string>` | no |
| `encryptPayload` | body | `boolean` | no |
| `includeVisualExperiments` | body | `boolean` | no |
| `includeDraftExperiments` | body | `boolean` | no |
| `includeExperimentNames` | body | `boolean` | no |
| `includeRedirectExperiments` | body | `boolean` | no |
| `includeRuleIds` | body | `boolean` | no |
| `includeProjectIdInMetadata` | body | `boolean` | no |
| `includeCustomFieldsInMetadata` | body | `boolean` | no |
| `allowedCustomFieldsInMetadata` | body | `list<string>` | no |
| `includeTagsInMetadata` | body | `boolean` | no |
| `proxyEnabled` | body | `boolean` | no |
| `proxyHost` | body | `string` | no |
| `hashSecureAttributes` | body | `boolean` | no |
| `remoteEvalEnabled` | body | `boolean` | no |
| `savedGroupReferencesEnabled` | body | `boolean` | no |
