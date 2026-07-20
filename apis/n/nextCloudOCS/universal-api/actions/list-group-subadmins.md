# Next Cloud OCS: List Group Subadmins

Retrieves group subadmins from Next Cloud OCS.

```
GET https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-group-subadmins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-group-subadmins?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-group-subadmins?${params}`, {
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
      "data": {},
      "message": "string",
      "ocs": {},
      "status": "string",
      "statuscode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Primary response payload returned by the endpoint. |
| `message` | string | Human-readable status or error message when provided. |
| `ocs` | object | OCS metadata wrapper returned by Nextcloud. |
| `status` | string | Endpoint status value when provided. |
| `statuscode` | number | Nextcloud OCS status code when provided. |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `GET /ocs/v2.php/cloud/groups/{{groupId}}/subadmins` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-subadmins.md) for the provider-specific parameters and requirements.

