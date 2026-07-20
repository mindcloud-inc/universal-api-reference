# MOBIDI: Check Sync Health

Retrieves sync health details from MOBIDI.

```
GET https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/check-sync-health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/check-sync-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/check-sync-health?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MOBIDI API returns.

## Native endpoint

Through the native MOBIDI API, this operation is `GET /MobidiServerSyncHandler?loginWithGuest=1` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-sync-health.md) for the provider-specific parameters and requirements.

