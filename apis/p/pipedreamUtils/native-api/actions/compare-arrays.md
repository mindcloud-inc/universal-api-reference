# Helper Functions - Compare Arrays with Pipedream Utils

Compares two arrays or sets in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Helper Functions - Compare Arrays](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/compare-arrays/compare-arrays.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `array1` | body | `list<string>` | yes | Array to compare to second array Send multiple values as a array. |
| `array2` | body | `list<string>` | yes | Array to be compared with first array Send multiple values as a array. |
| `actionType` | body | `string` | yes | Type of action to perform on the arrays |
