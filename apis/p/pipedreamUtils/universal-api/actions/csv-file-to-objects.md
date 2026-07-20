# Pipedream Utils: Helper Functions - CSV File To Objects

Converts a /tmp CSV file to objects in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/csv-file-to-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/csv-file-to-objects?connectionId=$CONNECTION_ID&filePath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filePath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/csv-file-to-objects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filePath` | string | yes | The path to the file saved to the `/tmp` directory (e.g. `/tmp/example.csv`). [See the documentation](https://pipedream.com/docs/workflows/steps/code/nodejs/working-with-files/#the-tmp-directory). |
| `hasHeaders` | boolean | no | Set to `true` if the first row of the CSV contains headers. If there are headers in the file, the keys of the objects will be the header values. If there are no headers, each object will be an array of values. |
| `skipEmptyLines` | boolean | no | Set to `true` to skip empty lines in the file. |
| `skipRecordsWithEmptyValues` | boolean | no | Set to `true` to skip records with empty values. Don't generate records for lines containing empty values, empty Buffer or equals to `null` and `undefined` if their value was casted. |
| `skipRecordsWithError` | boolean | no | Set to `true` to skip records with errors. Tolerates parsing errors. It skips the records containing an error inside and directly go process the next record. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedream Utils API returns.

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/csv-file-to-objects.md) for the provider-specific parameters and requirements.

