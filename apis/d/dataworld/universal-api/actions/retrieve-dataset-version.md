# data.world: Retrieve a Dataset Version

Retrieves a dataset version from data.world.

```
GET https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/retrieve-dataset-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a data.world `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/retrieve-dataset-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/retrieve-dataset-version?${params}`, {
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
      "id": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `updated` | date |  |
| `versionId` | string |  |

## Native endpoint

Through the native data.world API, this operation is `GET /datasets/{owner}/{id}/v/{versionId}` (base URL `https://api.data.world/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-dataset-version.md) for the provider-specific parameters and requirements.

