# Agify: Predict Ages



```
GET https://connect.mindcloud.co/v1/universal/agify/latest/actions/predict-ages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agify/latest/actions/predict-ages?connectionId=$CONNECTION_ID&names%5B%5D=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "names[]": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agify/latest/actions/predict-ages?${params}`, {
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
| `names[]` | array<string> | yes | Up to 10 names to predict in one request. Accepts multiple values as an array. |
| `country_id` | string | no | Optional ISO 3166-1 alpha-2 country code to scope every prediction in the batch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agify API returns.

## Native endpoint

Through the native Agify API, this operation is `GET /` (base URL `https://api.agify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/predict-ages.md) for the provider-specific parameters and requirements.

