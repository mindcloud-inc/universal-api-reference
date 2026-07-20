# Dwolla: Get Account

Retrieves details for a Dwolla account.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-account?${params}`, {
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
| `id` | string | no | Dwolla account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "id": "string",
      "name": "Ava Chen",
      "timezoneOffset": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for related account resources. |
| `id` | string | Dwolla account identifier. |
| `name` | string | Display name of the main account. |
| `timezoneOffset` | number | Account timezone offset in hours from UTC. |
| `type` | string | Dwolla account type. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /accounts/[:id]` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

