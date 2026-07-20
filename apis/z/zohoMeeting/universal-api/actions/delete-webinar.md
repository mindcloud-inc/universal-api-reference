# Zoho Meeting: Delete Webinar

Deletes an existing webinar from Zoho Meeting.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/delete-webinar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/delete-webinar?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D&webinarKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/delete-webinar?${params}`, {
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
| `organizationId` | string | yes | Organization ID (zsoid) from Get Current User Details. Default: `{{credentials.organizationId}}`. |
| `webinarKey` | string | yes | Webinar key returned by List Webinars or Create Webinar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `DELETE /api/v2/:organizationId/webinar/:webinarKey.json` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webinar.md) for the provider-specific parameters and requirements.

