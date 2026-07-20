# Filestage: Get Review Decision Count

Retrieves review decision counts from a Filestage section.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-review-decision-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-review-decision-count?connectionId=$CONNECTION_ID&sectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-review-decision-count?${params}`, {
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
| `sectionId` | string | yes | Section Id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reviewsCount": {
        "APPROVED": 1,
        "DECLINED": 1,
        "NO_REVIEWS": 1
      },
      "sectionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reviewsCount` | object |  |
| `reviewsCount.APPROVED` | number |  |
| `reviewsCount.DECLINED` | number |  |
| `reviewsCount.NO_REVIEWS` | number |  |
| `sectionId` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `GET /sections/{sectionId}/reviews/status/count` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-review-decision-count.md) for the provider-specific parameters and requirements.

