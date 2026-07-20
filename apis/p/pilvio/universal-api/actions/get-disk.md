# Pilvio: Get Disk



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-disk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-disk?connectionId=$CONNECTION_ID&diskUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "diskUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-disk?${params}`, {
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
| `diskUuid` | string | yes | UUID of the disk to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "snapshots": [
        {
          "sizeGb": 1,
          "uuid": "string"
        }
      ],
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `snapshots[].sizeGb` | number |  |
| `snapshots[].uuid` | string |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /storage/disks/{disk_uuid}` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-disk.md) for the provider-specific parameters and requirements.

