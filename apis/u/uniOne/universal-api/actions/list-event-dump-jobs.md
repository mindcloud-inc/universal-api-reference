# UniOne: List Event Dump Jobs

Retrieves event dump jobs from UniOne.

```
GET https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-event-dump-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-event-dump-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-event-dump-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "event_dumps": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_dumps` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native UniOne API, this operation is `POST event-dump/list.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-dump-jobs.md) for the provider-specific parameters and requirements.

