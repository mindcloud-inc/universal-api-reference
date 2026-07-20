# Signaturit: List Event Hooks

Retrieves event hooks from Signaturit.

```
GET https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-event-hooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-event-hooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-event-hooks?${params}`, {
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
| `page` | number | no | Page number to fetch. Defaults to 1. Default: `1`. Example: `1`. |
| `status` | list<number> | no | One or more event-hook HTTP status codes to match. Accepts multiple values as an array. Example: `200`. |
| `method` | list<string> | no | One or more HTTP methods to match, for example POST or GET. Accepts multiple values as an array. Example: `POST`. |
| `search` | string | no | Search string to match event-hook records. Example: `email_`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | no | Stringified JSON date range like {"from":"2023-03-01","to":"2023-03-28"}. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |

## Native endpoint

Through the native Signaturit API, this operation is `GET /event-hooks` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-hooks.md) for the provider-specific parameters and requirements.

