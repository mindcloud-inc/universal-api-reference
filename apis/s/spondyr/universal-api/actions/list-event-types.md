# Spondyr: List Event Types

Retrieves event types for a transaction type in Spondyr.

```
GET https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-event-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spondyr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-event-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-event-types?${params}`, {
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
| `transactionType` | string | no | Optional transaction type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "APIStatus": "string",
      "Data": [
        {}
      ],
      "ErrorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `APIStatus` | string |  |
| `Data` | array<object> | Event types returned by Spondyr. |
| `ErrorMessage` | string |  |

## Native endpoint

Through the native Spondyr API, this operation is `GET /EventTypes` (base URL `https://client.spondyr.io/api/v1.0.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-types.md) for the provider-specific parameters and requirements.

