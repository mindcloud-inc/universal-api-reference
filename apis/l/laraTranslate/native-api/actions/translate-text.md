# Translate text with Lara Translate

Translates text from one language to another in Lara Translate.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://mcp-v2.laratranslate.com/v1`
- **Official documentation:** [Translate text](https://developers.laratranslate.com/docs/translate-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text[]` | body | `array<object>` | yes | Array of text blocks to translate. Each item should include text and a translatable boolean. |
| `source` | body | `string` | no | Optional source language code such as en-US. |
| `target` | body | `string` | yes | Target language code such as it-IT. |
| `context` | body | `string` | no | Optional context to improve translation quality. |
| `instructions[]` | body | `array<string>` | no | Optional list of short localization directives. |
| `source_hint` | body | `string` | no | Optional language hint to guide detection. |
| `adapt_to[]` | body | `array<string>` | no | Optional list of translation memory IDs to adapt to. |
| `style` | body | `list` | no | Optional translation style. Accepted values: `Creative`, `Faithful`, `Fluid`. |
| `reasoning` | body | `boolean` | no | Whether to include reasoning in the translation response. |
| `content_type` | body | `list` | no | Content type of the source text. Accepted values: `HTML`, `Plain text`, `XLIFF`. |
| `no_trace` | body | `boolean` | no | If true, Lara does not store the translation in logs. |
| `priority` | body | `list` | no | Optional translation request priority. Accepted values: `Background`, `Normal`. |
| `timeout_in_millis` | body | `number` | no | Custom timeout for the translation request in milliseconds. Maximum 300000. |
