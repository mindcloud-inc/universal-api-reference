# Synchroteam: Search Jobs

Finds jobs in Synchroteam using supported search filters.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-jobs?${params}`, {
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
| `filters` | object | no | Optional. Provide the Synchroteam job search filters object (per docs). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "myId": "string",
      "num": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `myId` | string |  |
| `num` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `POST /Api/v2/Jobs/Search` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-jobs.md) for the provider-specific parameters and requirements.

