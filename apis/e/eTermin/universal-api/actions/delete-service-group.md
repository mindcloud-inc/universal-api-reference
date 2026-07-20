# eTermin: Delete Service Group

Deletes an existing service group from eTermin.

```
DELETE https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-service-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-service-group?connectionId=$CONNECTION_ID&servicegroupid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "servicegroupid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-service-group?${params}`, {
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
| `servicegroupid` | number | yes | ID of the servicegroup that you want information on |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "statusMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `statusMsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `DELETE /api/servicegroup` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-service-group.md) for the provider-specific parameters and requirements.

