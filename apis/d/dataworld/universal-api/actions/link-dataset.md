# data.world: Link Dataset

Links a dataset to a project in data.world.

```
PUT https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/link-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a data.world `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/link-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/link-dataset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "linkedDatasetId": "https://example.com",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `linkedDatasetId` | string |  |
| `projectId` | string |  |

## Native endpoint

Through the native data.world API, this operation is `PUT /projects/{owner}/{id}/linkedDatasets/{linkedDatasetOwner}/{linkedDatasetId}` (base URL `https://api.data.world/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-dataset.md) for the provider-specific parameters and requirements.

