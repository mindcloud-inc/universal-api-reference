# Apify: Get Dataset

Retrieves a dataset from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-dataset?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-dataset?${params}`, {
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
| `datasetId` | string | yes | The ID of the dataset to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accessedAt": "2026-05-07T12:00:00.000Z",
        "actId": {},
        "actRunId": {},
        "cleanItemCount": 1,
        "consoleUrl": "https://example.com",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "fields": [
          "string"
        ],
        "generalAccess": "string",
        "id": "string",
        "itemCount": 1,
        "itemsPublicUrl": "https://example.com",
        "modifiedAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "schema": {},
        "stats": {
          "readCount": 1,
          "storageBytes": 1,
          "writeCount": 1
        },
        "urlSigningSecretKey": "https://example.com",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.accessedAt` | date |  |
| `data.actId` | object |  |
| `data.actRunId` | object |  |
| `data.cleanItemCount` | number |  |
| `data.consoleUrl` | string |  |
| `data.createdAt` | date |  |
| `data.fields[]` | string |  |
| `data.generalAccess` | string |  |
| `data.id` | string |  |
| `data.itemCount` | number |  |
| `data.itemsPublicUrl` | string |  |
| `data.modifiedAt` | date |  |
| `data.name` | string |  |
| `data.schema` | object |  |
| `data.stats.readCount` | number |  |
| `data.stats.storageBytes` | number |  |
| `data.stats.writeCount` | number |  |
| `data.urlSigningSecretKey` | string |  |
| `data.userId` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/datasets/:datasetId` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset.md) for the provider-specific parameters and requirements.

