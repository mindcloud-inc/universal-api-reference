# Draftable: Get Comparison

Retrieves a document comparison from Draftable.

```
GET https://connect.mindcloud.co/v1/universal/draftable/latest/actions/get-comparison
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Draftable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/get-comparison?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/draftable/latest/actions/get-comparison?${params}`, {
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
| `identifier` | string | yes | The comparison identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comparisonType": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "failed": true,
      "identifier": "string",
      "left": {
        "fileType": "string",
        "pageCount": 1,
        "sourceUrl": "https://example.com"
      },
      "public": true,
      "ready": true,
      "readyTime": "2026-05-07T12:00:00.000Z",
      "right": {
        "fileType": "string",
        "pageCount": 1,
        "sourceUrl": "https://example.com"
      },
      "viewerUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comparisonType` | string |  |
| `creationTime` | date |  |
| `failed` | boolean |  |
| `identifier` | string |  |
| `left.fileType` | string |  |
| `left.pageCount` | number |  |
| `left.sourceUrl` | string |  |
| `public` | boolean |  |
| `ready` | boolean |  |
| `readyTime` | date |  |
| `right.fileType` | string |  |
| `right.pageCount` | number |  |
| `right.sourceUrl` | string |  |
| `viewerUrl` | string |  |

## Native endpoint

Through the native Draftable API, this operation is `GET /comparisons/{{identifier}}` (base URL `https://api.draftable.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comparison.md) for the provider-specific parameters and requirements.

