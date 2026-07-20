# Sendible: Get Campaign Posts Report



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-campaign-posts-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-campaign-posts-report?connectionId=$CONNECTION_ID&campaignId=1&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1",
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-campaign-posts-report?${params}`, {
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
| `campaignId` | number | yes | Campaign ID. |
| `orderBy` | string | no | Optional sort field. |
| `page` | number | yes | Page number. Default: `1`. |
| `socialNetwork` | string | no | Optional social network filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Sendible API, this operation is `GET 1.0/api/campaign/report/posts` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-posts-report.md) for the provider-specific parameters and requirements.

