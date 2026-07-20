# Novofon: Get Direct Number

Retrieves a direct number from Novofon.

```
GET https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-direct-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-direct-number?connectionId=$CONNECTION_ID&number=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-direct-number?${params}`, {
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
| `number` | string | yes | Purchased direct number to inspect. |
| `type` | string | yes | Number type. Docs say `revenue` for free Moscow 495 numbers and `common` for regular numbers. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Novofon API returns.

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/direct_numbers/number/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-direct-number.md) for the provider-specific parameters and requirements.

