# serviceminder.io: List Services

Retrieves services from ServiceMinder.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-services?${params}`, {
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
| `includeInactive` | boolean | no | Whether to include inactive services. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "includeInactive": true,
      "includeParts": true,
      "matches": [
        {}
      ],
      "message": "string",
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `includeInactive` | boolean |  |
| `includeParts` | boolean |  |
| `matches` | array<object> |  |
| `message` | string |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /services/all` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

