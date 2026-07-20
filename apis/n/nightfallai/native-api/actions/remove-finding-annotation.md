# Remove Finding Annotation with Nightfall.ai

Deletes a finding annotation from Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/dlp/v1/findings/:findingId/unannotate`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Remove Finding Annotation](https://help.nightfall.ai/developer-api/nightfall_apis/saas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `findingId` | path | `string` | yes | The UUID of the finding whose annotation should be removed. |
