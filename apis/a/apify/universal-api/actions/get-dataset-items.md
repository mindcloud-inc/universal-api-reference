# Apify: Get Dataset Items

Retrieves items from an Apify dataset.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-dataset-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-dataset-items?connectionId=$CONNECTION_ID&limit=25&offset=0&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-dataset-items?${params}`, {
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
| `datasetId` | string | yes | The ID of the dataset whose items to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "source": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `source` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/datasets/:datasetId/items` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-dataset-items.md) for the provider-specific parameters and requirements.

