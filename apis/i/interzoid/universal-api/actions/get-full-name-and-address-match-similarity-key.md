# Interzoid: Get Full Name And Address Match Similarity Key



```
GET https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-full-name-and-address-match-similarity-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Interzoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-full-name-and-address-match-similarity-key?connectionId=$CONNECTION_ID&address=string&fullname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string",
  "fullname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-full-name-and-address-match-similarity-key?${params}`, {
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
| `address` | string | yes | Street address to encode. |
| `fullname` | string | yes | Full name to encode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "Credits": "string",
      "SimKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string |  |
| `Credits` | string |  |
| `SimKey` | string |  |

## Native endpoint

Through the native Interzoid API, this operation is `GET /getaddressandfullnamematch` (base URL `https://api.interzoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-name-and-address-match-similarity-key.md) for the provider-specific parameters and requirements.

