# Transform Case with Formatting

Transforms text case in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Transform Case](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/transform-case/transform-case.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The text to transform. |
| `operationMode` | body | `string` | yes | The case format to apply. |
