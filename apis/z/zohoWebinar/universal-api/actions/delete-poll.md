# Zoho Webinar: Delete Poll

Deletes an existing webinar poll from Zoho Webinar.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/delete-poll
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/delete-poll?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D&pollId=string&webinarKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}",
  "pollId": "string",
  "webinarKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/delete-poll?${params}`, {
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
| `organizationId` | string | yes | Default: `{{credentials.organizationId}}`. |
| `pollId` | string | yes |  |
| `webinarKey` | string | yes |  |
| `instanceId` | string | no |  |

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

Through the native Zoho Webinar API, this operation is `DELETE /meeting/api/v2/:organizationId/poll/:pollId` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-poll.md) for the provider-specific parameters and requirements.

