# Pushbullet: Delete All Pushes

Deletes all pushes from your Pushbullet account.

```
DELETE https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-all-pushes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-all-pushes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-all-pushes?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Pushbullet API, this operation is `DELETE /pushes` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-all-pushes.md) for the provider-specific parameters and requirements.

