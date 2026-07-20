# PrintNode: List Computers by Set

Retrieves specific computers from PrintNode by ID set.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-computers-by-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-computers-by-set?connectionId=$CONNECTION_ID&computerSet=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "computerSet": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-computers-by-set?${params}`, {
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
| `computerSet` | string | yes | Comma-separated PrintNode computer IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTimestamp": "2026-05-07T12:00:00.000Z",
      "hostname": "Ava Chen",
      "id": 1,
      "inet": "string",
      "inet6": "string",
      "jre": "string",
      "name": "Ava Chen",
      "state": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTimestamp` | date | Timestamp when the computer was first registered. |
| `hostname` | string | Computer host name. |
| `id` | number | Computer identifier. |
| `inet` | string | IPv4 address reported by the client. |
| `inet6` | string | IPv6 address reported by the client. |
| `jre` | string | Java runtime version when present. |
| `name` | string | Computer name reported by PrintNode. |
| `state` | string | Computer connection state. |
| `version` | string | PrintNode client version. |

## Native endpoint

Through the native PrintNode API, this operation is `GET /computers/:computerSet` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-computers-by-set.md) for the provider-specific parameters and requirements.

