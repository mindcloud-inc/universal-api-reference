# Archive Interview with Hireflix

Archives or restores an interview in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [Archive Interview](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Hireflix interview ID. |
| `variables.archive` | body | `boolean` | no | Whether the interview should be archived. |
