# Bluebarry: List Settings

Retrieves settings entity records from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-settings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-settings?${params}`, {
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
      "allowOverage": true,
      "analyticsPropertyId": "string",
      "availableLanguages": [
        "string"
      ],
      "clonedFrom": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "id": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifierId": "string",
      "reference": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowOverage` | boolean |  |
| `analyticsPropertyId` | string |  |
| `availableLanguages` | array<string> |  |
| `clonedFrom` | string |  |
| `createdDate` | date |  |
| `creatorId` | string |  |
| `id` | string |  |
| `modifiedDate` | date |  |
| `modifierId` | string |  |
| `reference` | string |  |
| `tenantId` | string |  |

## Native endpoint

Through the native Bluebarry API, this operation is `GET /data/Settings` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-settings.md) for the provider-specific parameters and requirements.

