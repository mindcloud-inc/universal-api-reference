# Countly: List Push Messages

Retrieves all push messages from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-push-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-push-messages?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-push-messages?${params}`, {
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
| `appId` | string | yes | Countly app ID to list push messages for. |
| `source` | string | no | Push source filter, such as api or dash. |
| `sSearch` | string | no | Search text for the default message. |
| `iDisplayStart` | number | no | Number of push records to skip. |
| `iDisplayLength` | number | no | Number of push records to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `iSortCol0` | string | no | Column to sort push messages by. |
| `sSortDir0` | string | no | Sort direction, asc or desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aaData": [
        {}
      ],
      "iTotalDisplayRecords": 1,
      "iTotalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aaData` | array<object> |  |
| `iTotalDisplayRecords` | number |  |
| `iTotalRecords` | number |  |

## Native endpoint

Through the native Countly API, this operation is `GET /o/pushes/all` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-push-messages.md) for the provider-specific parameters and requirements.

