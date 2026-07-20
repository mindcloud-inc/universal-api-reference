# Apply Media Pattern with Pirsonal

Applies a pattern to existing media in Pirsonal.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Apply Media Pattern](https://app.pirsonal.com/docAPI#Media_Apply_Pattern)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaID` | body | `string` | yes | ID of the media to transform. |
| `patter` | body | `list<string>` | yes | Pattern type. Pirsonal docs list `audiolevel`. Accepted values: `audiolevel`. |
| `action` | body | `list<string>` | yes | Pattern action: info, one, or multi. Accepted values: `info`, `multi`, `one`. |
| `parameters` | body | `string` | yes | Stringified JSON parameters for the selected pattern, for example an audiolevel threshold object. |
