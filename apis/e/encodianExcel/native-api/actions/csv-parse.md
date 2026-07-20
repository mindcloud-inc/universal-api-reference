# CSV - Parse with Encodian - Excel

Parses a CSV file into JSON in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ParseCsv`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [CSV - Parse](https://support.encodian.com/hc/en-gb/articles/360005177297-Parse-CSV)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `file` | yes | The file content of the source CSV file. |
| `delimiter` | body | `string` | no | Set the CSV delimiter. Defaults to comma. |
| `encoding` | body | `list<string>` | no | Accepted values: `ASCII`, `ISO88591`, `ISO88592`, `Latin1`, `UTF8`. |
| `csvColumnHeaders` | body | `string` | no | Optional comma-delimited column headers. |
| `skipFirstLine` | body | `boolean` | no | Skip the first line when the CSV contains headers. |
