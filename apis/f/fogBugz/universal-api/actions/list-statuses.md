# FogBugz: List Statuses

Retrieves statuses from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-statuses?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ixCategory` | number | no | Return statuses for a specific category. |
| `fResolved` | boolean | no | Set to true to return only resolved statuses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fDeleted": true,
      "fDuplicate": true,
      "fReactivate": true,
      "fResolved": true,
      "fWorkDone": true,
      "iOrder": 1,
      "ixCategory": 1,
      "ixStatus": 1,
      "sStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fDeleted` | boolean | Whether the status is deleted. |
| `fDuplicate` | boolean | Whether the status marks duplicates. |
| `fReactivate` | boolean | Whether the status allows reactivation. |
| `fResolved` | boolean | Whether the status is resolved. |
| `fWorkDone` | boolean | Whether the status counts as work done. |
| `iOrder` | number | Display order. |
| `ixCategory` | number | Category ID. |
| `ixStatus` | number | Status ID. |
| `sStatus` | string | Status name. |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listStatuses` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-statuses.md) for the provider-specific parameters and requirements.

