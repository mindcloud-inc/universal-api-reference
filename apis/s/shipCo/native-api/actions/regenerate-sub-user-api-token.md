# Regenerate Sub User API Token with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/sub-users/:id`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Regenerate Sub User API Token](https://developer.shipandco.com/en/#sub-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ship&Co sub-user ID whose token should be regenerated. Ship&Co requires a 32-character sub-user ID. Maximum length: 32. |
