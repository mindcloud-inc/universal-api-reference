# Helper Functions - CSV File To Objects with Pipedream Utils

Converts a /tmp CSV file to objects in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Helper Functions - CSV File To Objects](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/csv-file-to-objects/csv-file-to-objects.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filePath` | body | `string` | yes | The path to the file saved to the `/tmp` directory (e.g. `/tmp/example.csv`). [See the documentation](https://pipedream.com/docs/workflows/steps/code/nodejs/working-with-files/#the-tmp-directory). |
| `hasHeaders` | body | `boolean` | no | Set to `true` if the first row of the CSV contains headers. If there are headers in the file, the keys of the objects will be the header values. If there are no headers, each object will be an array of values. |
| `skipEmptyLines` | body | `boolean` | no | Set to `true` to skip empty lines in the file. |
| `skipRecordsWithEmptyValues` | body | `boolean` | no | Set to `true` to skip records with empty values. Don't generate records for lines containing empty values, empty Buffer or equals to `null` and `undefined` if their value was casted. |
| `skipRecordsWithError` | body | `boolean` | no | Set to `true` to skip records with errors. Tolerates parsing errors. It skips the records containing an error inside and directly go process the next record. |
