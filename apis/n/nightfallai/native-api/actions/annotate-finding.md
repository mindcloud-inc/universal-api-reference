# Annotate Finding with Nightfall.ai

Updates a finding annotation in Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/dlp/v1/findings/:findingId/annotate`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Annotate Finding](https://help.nightfall.ai/developer-api/nightfall_apis/saas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `findingId` | path | `string` | yes | The UUID of the finding to annotate. |
| `type` | body | `string` | yes | Annotation type to apply. |
