# Pipedream Utils: Helper Functions - Get ISO String N Days Ago

Retrieves a UTC ISO timestamp from N days ago in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/get-iso-string-n-days-ago
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/get-iso-string-n-days-ago?connectionId=$CONNECTION_ID&days=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "days": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/get-iso-string-n-days-ago?${params}`, {
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
| `days` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-iso-string-n-days-ago.md) for the provider-specific parameters and requirements.

