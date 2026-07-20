# Categorize Content with WebCategorize

## Endpoint

- **Method:** `POST`
- **Path:** `/html`
- **Base URL:** `https://app.webcategorize.com/api`
- **Official documentation:** [Categorize Content](https://webcategorize.com/webcategorize.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | Plain text or HTML content to categorize. |
| `url` | body | `string` | no | Optional URL stored for reference; it is not used for classification. |
| `tags[]` | body | `array<string>` | no | Optional tags to store with the content submission. |
