# Algolia: Retrieve Index Settings

Retrieves all index settings from Algolia.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-index-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-index-settings?connectionId=$CONNECTION_ID&indexName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-index-settings?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributesForFaceting": [
        "string"
      ],
      "hitsPerPage": 1,
      "maxValuesPerFacet": 1,
      "paginationLimitedTo": 1,
      "ranking": [
        "string"
      ],
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributesForFaceting` | array<string> |  |
| `hitsPerPage` | number |  |
| `maxValuesPerFacet` | number |  |
| `paginationLimitedTo` | number |  |
| `ranking` | array<string> |  |
| `version` | number |  |

## Native endpoint

Through the native Algolia API, this operation is `GET /1/indexes/:indexName/settings` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-index-settings.md) for the provider-specific parameters and requirements.

