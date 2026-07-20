# Ubiqod by Skiply: Delete Badge List



```
DELETE https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/delete-badge-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/delete-badge-list?connectionId=$CONNECTION_ID&badgeListId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "badgeListId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/delete-badge-list?${params}`, {
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
| `badgeListId` | string | yes | Badge list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Deletion result message. |

## Native endpoint

Through the native Ubiqod by Skiply API, this operation is `DELETE /badges/:badgeListId` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-badge-list.md) for the provider-specific parameters and requirements.

