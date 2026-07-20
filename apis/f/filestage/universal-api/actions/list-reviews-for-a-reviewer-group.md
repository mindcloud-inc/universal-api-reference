# Filestage: List Reviews for a Reviewer Group

Retrieves reviews for a Filestage reviewer group.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-reviews-for-a-reviewer-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-reviews-for-a-reviewer-group?connectionId=$CONNECTION_ID&stepId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stepId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-reviews-for-a-reviewer-group?${params}`, {
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
| `stepId` | string | yes | The unique identifier of the Review Group. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | The maximum number of reviews to return. Defaults to 20. Default: `20`. |
| `orderBy` | string | no | The order in which to sort the reviews. Default: `NEWEST`. |
| `pageToken` | string | no | A token to retrieve the next page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "limit": 1,
        "nextPageToken": "string",
        "previousPageToken": "string"
      },
      "reviews": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `pagination.limit` | number |  |
| `pagination.nextPageToken` | string |  |
| `pagination.previousPageToken` | string |  |
| `reviews` | array<object> |  |

## Native endpoint

Through the native Filestage API, this operation is `GET /steps/{stepId}/reviews` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviews-for-a-reviewer-group.md) for the provider-specific parameters and requirements.

