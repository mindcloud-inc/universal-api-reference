# Fivetran: Get Destination

Retrieves a destination from your Fivetran account.

```
GET https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-destination?connectionId=$CONNECTION_ID&destinationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "destinationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-destination?${params}`, {
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
| `destinationId` | string | yes | The unique identifier for the destination within Fivetran. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "groupId": "string",
      "id": "string",
      "region": "string",
      "service": "string",
      "setupStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `groupId` | string |  |
| `id` | string |  |
| `region` | string |  |
| `service` | string |  |
| `setupStatus` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `GET /destinations/[:destinationId]` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-destination.md) for the provider-specific parameters and requirements.

