# Cisco Webex Meetings: List Meetings

Retrieves meetings from Cisco Webex Meetings.

```
GET https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/list-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cisco Webex Meetings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/list-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/list-meetings?${params}`, {
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
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> | List of meetings returned by the Webex List Meetings endpoint. |

## Native endpoint

Through the native Cisco Webex Meetings API, this operation is `GET /meetings` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meetings.md) for the provider-specific parameters and requirements.

