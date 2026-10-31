# Set Project Fields with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:id/project-fields`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set Project Fields](https://developers.gobridgit.com/reference/projectfields_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Account ID |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].id` | body | `number` | yes | — |
| `payload[].name` | body | `string` | yes | — |
| `payload[].type` | body | `list<string>` | yes | Accepted values: `Address`, `Boolean`, `Currency`, `Date`, `Email`, `Image`, `Integer`, `LongText`, `MultiSelect`, `Number`, `Phone`, `SingleSelect`, `Text`. |
| `payload[].definedValues[]` | body | `array<object>` | no | — |
| `payload[].definedValues[].valueId` | body | `number` | yes | — |
| `payload[].definedValues[].definedValue` | body | `string` | yes | — |
| `payload[].definedValues[].forRemoval` | body | `boolean` | yes | — |
| `payload[].definedValues[].deleteExperienceFieldValues` | body | `boolean` | yes | — |
| `payload[].definedValues[].isHidden` | body | `boolean` | no | Null or omitted leaves the stored state unchanged. |
| `payload[].definedValues[].parentId` | body | `number` | no | Id of the parent defined value for title hierarchy. Null or omitted leaves the stored parent unchanged; send 0 to clear it (make the value a root). |
| `payload[].isRequired` | body | `boolean` | yes | — |
| `payload[].isPrivate` | body | `boolean` | yes | — |
| `payload[].isLocked` | body | `boolean` | yes | — |
