# Algolia: Delete Records Matching a Filter

Deletes records matching a filter in Algolia.

```
DELETE https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-records-matching-a-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-records-matching-a-filter?connectionId=$CONNECTION_ID&indexName=Ava%20Chen&filters=category%3Afootwear" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen",
  "filters": "category:footwear"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-records-matching-a-filter?${params}`, {
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
| `indexName` | string | yes | The name of the Algolia index. |
| `filters` | string | yes | Filter expression that selects the records to delete. Example: `category:footwear`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskID": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskID` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/deleteByQuery` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records-matching-a-filter.md) for the provider-specific parameters and requirements.

