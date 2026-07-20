# Pilvio: List VMs



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-vms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-vms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-vms?${params}`, {
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
      "backup": true,
      "billingAccount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hostname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backup` | boolean |  |
| `billingAccount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `hostname` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /user-resource/vm/list` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vms.md) for the provider-specific parameters and requirements.

