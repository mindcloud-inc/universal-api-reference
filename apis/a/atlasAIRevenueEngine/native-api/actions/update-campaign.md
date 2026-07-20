# Update Campaign with Atlas AI Revenue Engine

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaign/:id`
- **Base URL:** `https://api.youratlas.com/v1/api`
- **Official documentation:** [Update Campaign](https://apidocs.youratlas.com/update-campaign-26754245e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The campaign ID. |
| `campaignId` | body | `string` | no | Optional campaign identifier in the request body. |
| `AgentTypeName` | body | `string` | no | Agent type name. |
| `Language` | body | `string` | no | Agent language. |
| `Name` | body | `string` | no | Campaign or agent display name. |
| `PostScript` | body | `string` | no | Post-script text. |
| `PreScript` | body | `string` | no | Pre-script text. |
| `VoiceId` | body | `string` | no | Voice identifier. |
| `Model` | body | `string` | no | Voice model. |
| `Provider` | body | `string` | no | Voice provider. |
| `Stability` | body | `number` | no | Voice stability setting. |
| `SimilarityBoost` | body | `number` | no | Voice similarity boost setting. |
| `BackgroundSound` | body | `string` | no | Background sound setting. |
| `AtlasVoiceId` | body | `string` | no | Atlas voice identifier. |
| `Pitch` | body | `number` | no | Voice pitch setting. |
| `Gender` | body | `string` | no | Voice gender. |
| `Speed` | body | `number` | no | Voice speed setting. |
| `Slug` | body | `string` | no | Campaign slug. |
| `LanguageBoost` | body | `string` | no | Language boost setting. |
| `TextNormalizationEnabled` | body | `boolean` | no | Whether text normalization is enabled. |
| `Region` | body | `string` | no | Voice region. |
| `Volume` | body | `number` | no | Voice volume setting. |
| `FillerInjectionEnabled` | body | `boolean` | no | Whether filler injection is enabled. |
