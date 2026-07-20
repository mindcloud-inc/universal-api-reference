# Synchroteam: Search Activities

Finds activities in Synchroteam using supported search filters.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-activities?${params}`, {
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
| `filters` | object | no | Optional. Provide the Synchroteam activity search filters object (per docs). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityType": {
        "id": 1,
        "name": "Ava Chen"
      },
      "dateEnd": "string",
      "dateStart": "string",
      "id": 1,
      "note": "string",
      "user": {
        "id": 1,
        "login": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityType.id` | number |  |
| `activityType.name` | string |  |
| `dateEnd` | string |  |
| `dateStart` | string |  |
| `id` | number |  |
| `note` | string |  |
| `user.id` | number |  |
| `user.login` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `POST /Api/v2/Activities/Search` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-activities.md) for the provider-specific parameters and requirements.

