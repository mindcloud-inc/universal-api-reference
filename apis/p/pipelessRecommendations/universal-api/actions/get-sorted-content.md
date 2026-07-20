# Pipeless Recommendations: Get Sorted Content

Ranks supplied content in Pipeless Recommendations for a target object.

```
GET https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-sorted-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeless Recommendations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-sorted-content?connectionId=$CONNECTION_ID&appId=1885&object.id=3507&object.type=user&primaryPositiveRelationshipType=liked&contentTaggedRelationshipType=categorizedIn&contentTagObjectType=category&contentObjectType=company&contentIds%5B0%5D=Rosita's%20Place&contentIds%5B1%5D=Noodle%20Bar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1885",
  "object.id": "3507",
  "object.type": "user",
  "primaryPositiveRelationshipType": "liked",
  "contentTaggedRelationshipType": "categorizedIn",
  "contentTagObjectType": "category",
  "contentObjectType": "company",
  "contentIds[0]": "Rosita's Place",
  "contentIds[1]": "Noodle Bar"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-sorted-content?${params}`, {
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
| `appId` | string | yes | Numeric Pipeless app ID. Default: `1885`. |
| `object.id` | string | yes | Default: `3507`. |
| `object.type` | string | yes | Default: `user`. |
| `primaryPositiveRelationshipType` | string | yes | Default: `liked`. |
| `contentTaggedRelationshipType` | string | yes | Default: `categorizedIn`. |
| `contentTagObjectType` | string | yes | Default: `category`. |
| `contentObjectType` | string | yes | Default: `company`. |
| `contentIds[0]` | string | yes | Default: `Rosita's Place`. |
| `contentIds[1]` | string | yes | Default: `Noodle Bar`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "object": {
            "createdOn": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "modifiedOn": "2026-05-07T12:00:00.000Z",
            "type": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].object.createdOn` | date |  |
| `items[].object.id` | string |  |
| `items[].object.modifiedOn` | date |  |
| `items[].object.type` | string |  |

## Native endpoint

Through the native Pipeless Recommendations API, this operation is `GET /v1/apps/:appId/algos/recommendations/sorted-content` (base URL `https://api.pipeless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sorted-content.md) for the provider-specific parameters and requirements.

