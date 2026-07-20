# Vybit: Get Peep



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-peep
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-peep?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-peep?${params}`, {
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
| `key` | string | yes | The unique key of the peep to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "key": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vybKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessStatus` | string | Access state for the subscription relationship. |
| `createdAt` | date | When the peep record was created. |
| `key` | string | Unique peep identifier. |
| `name` | string | Display name of the subscriber. |
| `updatedAt` | date | When the peep record was last updated. |
| `vybKey` | string | Key of the vybit this peep follows. |

## Native endpoint

Through the native Vybit API, this operation is `GET /peep/{{key}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-peep.md) for the provider-specific parameters and requirements.

