# Cisco Webex Meetings: Delete a Summary

Deletes an existing meeting summary from Cisco Webex Meetings.

```
DELETE https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cisco Webex Meetings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-summary?connectionId=$CONNECTION_ID&summaryId=a6d39d90-4f0e-4d4a-9d75-7932a69f2ff9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "summaryId": "a6d39d90-4f0e-4d4a-9d75-7932a69f2ff9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-summary?${params}`, {
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
| `summaryId` | string | yes | Unique identifier for the summary to delete. Example: `a6d39d90-4f0e-4d4a-9d75-7932a69f2ff9`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cisco Webex Meetings API returns.

## Native endpoint

Through the native Cisco Webex Meetings API, this operation is `DELETE /meetingSummaries/:summaryId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-summary.md) for the provider-specific parameters and requirements.

