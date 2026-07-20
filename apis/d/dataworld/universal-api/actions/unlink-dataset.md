# data.world: Unlink Dataset

Unlinks a dataset from a project in data.world.

```
DELETE https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/unlink-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a data.world `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/unlink-dataset?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/unlink-dataset?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
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
| `deleted` | boolean |  |
| `linkedDatasetId` | string |  |
| `projectId` | string |  |

## Native endpoint

Through the native data.world API, this operation is `DELETE /projects/{owner}/{id}/linkedDatasets/{linkedDatasetOwner}/{linkedDatasetId}` (base URL `https://api.data.world/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unlink-dataset.md) for the provider-specific parameters and requirements.

