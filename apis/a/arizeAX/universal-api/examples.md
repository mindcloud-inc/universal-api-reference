# Arize AX Universal API Examples

These examples use the MindCloud API key and Arize AX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Spaces

Retrieves spaces from Arize AX.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/list-spaces?${params}`, {
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
  "data": [
    {
      "pagination": {},
      "spaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Spaces action reference](actions/list-spaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/arizeAX/latest/actions/list-spaces).

## Add New Examples To A Dataset

Adds new examples to an existing dataset in Arize AX.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/add-new-examples-to-a-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string",
  "examples[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/add-new-examples-to-a-dataset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string",
    "examples[]": [{}]
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

See the full [Add New Examples To A Dataset action reference](actions/add-new-examples-to-a-dataset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/arizeAX/latest/actions/add-new-examples-to-a-dataset).
