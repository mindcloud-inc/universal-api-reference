# Hash Hidden Fields with Porsline

## Endpoint

- **Method:** `POST`
- **Path:** `/api/surveys/:survey_id/variables/hashes/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Hash Hidden Fields](https://developers.porsline.com/#tag/Hidden-Field-Encryption/paths/~1api~1surveys~1{survey_id}~1variables~1hashes~1/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `values` | body | `string` | yes | JSON array of respondent value maps to encrypt, for example [{"mc_stage3_var_1640":"alice@example.com"}] or [{"mc_stage3_var_1640":"alice@example.com","is_unique":true}]. |
