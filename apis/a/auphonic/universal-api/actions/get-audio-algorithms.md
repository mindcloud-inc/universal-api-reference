# Auphonic: Get Audio Algorithms

Retrieves audio algorithms from Auphonic.

```
GET https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-audio-algorithms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auphonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-audio-algorithms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-audio-algorithms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Auphonic API returns.

## Native endpoint

Through the native Auphonic API, this operation is `GET /info/algorithms.json` (base URL `https://auphonic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audio-algorithms.md) for the provider-specific parameters and requirements.

