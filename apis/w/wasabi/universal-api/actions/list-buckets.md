# Wasabi: List Buckets

Retrieves the buckets available in your Wasabi account.

```
GET https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-buckets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-buckets?${params}`, {
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
      "bucketRegion": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketRegion` | string | AWS/Wasabi region where the bucket is stored. |
| `creationDate` | date | Bucket creation timestamp. |
| `name` | string | Bucket name. |

## Native endpoint

Through the native Wasabi API, this operation is `GET /` (base URL `https://s3.wasabisys.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-buckets.md) for the provider-specific parameters and requirements.

