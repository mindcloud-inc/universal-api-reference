# MOBIDI: List Saved Queries

Retrieves saved user queries from MOBIDI.

```
GET https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/list-saved-queries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/list-saved-queries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/list-saved-queries?${params}`, {
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
      "IdSavedMobidiQuery": "string",
      "MobidiQuery": {},
      "QueryName": "Ava Chen",
      "UserEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IdSavedMobidiQuery` | string | Saved query identifier. |
| `MobidiQuery` | object | Saved MobidiQuery payload. |
| `QueryName` | string | Saved query name. |
| `UserEmail` | string | Email address that owns the saved query. |

## Native endpoint

Through the native MOBIDI API, this operation is `POST /MobidiQueryManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-saved-queries.md) for the provider-specific parameters and requirements.

