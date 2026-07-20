# SimFin: List SimFin bulk dataset metadata

Retrieves SimFin bulk dataset metadata.

```
GET https://connect.mindcloud.co/v1/universal/simFin/latest/actions/list-sim-fin-bulk-dataset-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimFin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simFin/latest/actions/list-sim-fin-bulk-dataset-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simFin/latest/actions/list-sim-fin-bulk-dataset-metadata?${params}`, {
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
      "access": "string",
      "availability": {},
      "dataset": "string",
      "fileSize": 1,
      "id": 1,
      "lastUpdated": [
        1
      ],
      "market": "string",
      "totalEntries": 1,
      "variant": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string | Access tier for this dataset availability row. |
| `availability` | object | Column availability counts keyed by column name. |
| `dataset` | string | Dataset key. |
| `fileSize` | number | Dataset file size in bytes. |
| `id` | number | SimFin metadata row identifier. |
| `lastUpdated` | array<number> | Last updated timestamp components returned by SimFin. |
| `market` | string | Market code when applicable. |
| `totalEntries` | number | Total rows available in the dataset file. |
| `variant` | string | Dataset variant when applicable. |

## Native endpoint

Through the native SimFin API, this operation is `GET info?type=datasets` (base URL `https://prod.simfin.com/api/bulk-download`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sim-fin-bulk-dataset-metadata.md) for the provider-specific parameters and requirements.

