# Ambee: Get Latest Air Quality By Postal Code

Retrieves latest air quality data in Ambee by postal code.

```
GET https://connect.mindcloud.co/v1/universal/ambee/latest/actions/get-latest-air-quality-by-postal-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ambee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ambee/latest/actions/get-latest-air-quality-by-postal-code?connectionId=$CONNECTION_ID&postalCode=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postalCode": "string",
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ambee/latest/actions/get-latest-air-quality-by-postal-code?${params}`, {
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
| `postalCode` | string | yes |  |
| `countryCode` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ambee API returns.

## Native endpoint

Through the native Ambee API, this operation is `GET /latest/by-postal-code` (base URL `https://api.ambeedata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-air-quality-by-postal-code.md) for the provider-specific parameters and requirements.

