# PrimeGate: List Contacts by Source



```
GET https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-contacts-by-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrimeGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-contacts-by-source?connectionId=$CONNECTION_ID&source=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-contacts-by-source?${params}`, {
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
| `source` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PrimeGate API returns.

## Native endpoint

Through the native PrimeGate API, this operation is `POST contact/get` (base URL `https://api.primegate.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts-by-source.md) for the provider-specific parameters and requirements.

