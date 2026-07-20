# Replace Text with Formatting

Replaces text in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Replace Text](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/replace-text/replace-text.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The source text. |
| `findText` | body | `string` | yes | The text or pattern to replace. |
| `replaceText` | body | `string` | yes | The replacement text. |
| `useRegex` | body | `boolean` | no | Whether to treat Find Text as a regular expression. |
