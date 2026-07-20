# Cituro: Get Ratings Summary

Retrieves the ratings summary from Cituro.

```
GET https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-ratings-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cituro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-ratings-summary?connectionId=$CONNECTION_ID&accountNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-ratings-summary?${params}`, {
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
| `accountNumber` | string | yes | The Cituro account number used in the ratings endpoint path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "average": 1,
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `average` | number | Average rating value across all ratings for the Cituro account. |
| `count` | number | Total number of ratings available for the Cituro account. |

## Native endpoint

Through the native Cituro API, this operation is `GET /ratings/:accountNumber/summary` (base URL `https://app.cituro.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ratings-summary.md) for the provider-specific parameters and requirements.

