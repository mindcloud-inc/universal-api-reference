# Galileo: Get Dataset Content

Retrieves content for a Galileo dataset.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-dataset-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-dataset-content?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-dataset-content?${params}`, {
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
| `datasetId` | string | yes | Galileo dataset UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnNames": [
        "Ava Chen"
      ],
      "limit": 1,
      "nextStartingToken": 1,
      "paginated": true,
      "rows": [
        {
          "index": 1,
          "metadata": {},
          "rowId": "string",
          "values": [
            "string"
          ],
          "valuesDict": {}
        }
      ],
      "startingToken": 1,
      "warningMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnNames` | array<string> |  |
| `limit` | number |  |
| `nextStartingToken` | number |  |
| `paginated` | boolean |  |
| `rows` | array<object> |  |
| `rows[].index` | number |  |
| `rows[].metadata` | object |  |
| `rows[].rowId` | string |  |
| `rows[].values` | array<string> |  |
| `rows[].valuesDict` | object |  |
| `startingToken` | number |  |
| `warningMessage` | string |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/datasets/:dataset_id/content` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset-content.md) for the provider-specific parameters and requirements.

