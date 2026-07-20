# Moosend: Delete Segment

Deletes an existing segment from Moosend.

```
DELETE https://connect.mindcloud.co/v1/universal/moosend/latest/actions/delete-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/delete-segment?connectionId=$CONNECTION_ID&mailingListId=string&segmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "string",
  "segmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/delete-segment?${params}`, {
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
| `mailingListId` | string | yes | The ID of the email list that contains the segment. |
| `segmentId` | string | yes | The ID of the segment to be deleted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Moosend API returns.

## Native endpoint

Through the native Moosend API, this operation is `DELETE /lists/{{MailingListID}}/segments/{{SegmentID}}/delete.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-segment.md) for the provider-specific parameters and requirements.

