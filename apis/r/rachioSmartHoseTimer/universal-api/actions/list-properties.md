# Rachio Smart Hose Timer: List Properties

Retrieves property records from your Rachio account.

```
GET https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-properties?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-properties?${params}`, {
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
| `userId` | string | yes | Rachio person ID for the property owner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "property": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `property` | array<object> | Properties for the requested user. |

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `GET https://cloud-rest.rach.io/property/listProperties/:userId` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

