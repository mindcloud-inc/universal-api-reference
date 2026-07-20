# Update Corpus with Vectara

Updates an existing corpus in Vectara.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/corpora/:corpus_key`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Update Corpus](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `enabled` | body | `boolean` | no | Whether the corpus is enabled. |
| `name` | body | `string` | no | Updated corpus name. |
| `description` | body | `string` | no | Updated corpus description. |
| `save_history` | body | `boolean` | no | Whether this corpus should save query history by default. |
