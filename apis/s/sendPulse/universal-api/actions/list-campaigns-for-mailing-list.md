# SendPulse: List Campaigns For Mailing List

Retrieves campaigns for a SendPulse mailing list.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-campaigns-for-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-campaigns-for-mailing-list?connectionId=$CONNECTION_ID&mailingListId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-campaigns-for-mailing-list?${params}`, {
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
| `mailingListId` | string | yes | The SendPulse mailing list identifier. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "task_id": 1,
      "task_name": "Ava Chen",
      "task_status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `task_id` | number |  |
| `task_name` | string |  |
| `task_status` | number |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /addressbooks/:mailingListId/campaigns` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns-for-mailing-list.md) for the provider-specific parameters and requirements.

