# Clarifai Universal API Examples

These examples use the MindCloud API key and Clarifai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Public Models

Retrieves public models from Clarifai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-public-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-public-models?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [List Public Models action reference](actions/list-public-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clarifai/latest/actions/list-public-models).

## Add Inputs To Dataset

Adds inputs to a dataset in Clarifai.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/add-inputs-to-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "datasetId": "string",
  "dataset_inputs[]": [
    {}
  ],
  "dataset_inputs[].input.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/add-inputs-to-dataset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "datasetId": "string",
    "dataset_inputs[]": [{}],
    "dataset_inputs[].input.id": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Inputs To Dataset action reference](actions/add-inputs-to-dataset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clarifai/latest/actions/add-inputs-to-dataset).
