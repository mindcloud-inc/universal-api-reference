# LoginRadius: Delete Custom Object by ID

Deletes an existing custom object from LoginRadius by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-custom-object-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-custom-object-by-id?connectionId=$CONNECTION_ID&objectRecordId=record-1&accessToken=seeded-access-token&objectName=profileNote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectRecordId": "record-1",
  "accessToken": "seeded-access-token",
  "objectName": "profileNote"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-custom-object-by-id?${params}`, {
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
| `objectRecordId` | string | yes | Record identifier of the custom object entry to delete. Example: `record-1`. |
| `accessToken` | string | yes | Access Token of the user owning the custom object record. Example: `seeded-access-token`. |
| `objectName` | string | yes | Custom object name configured in LoginRadius. Example: `profileNote`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customObjectId` | string | no | Custom object schema identifier when required by the tenant. Example: `profileNote-1`. |
| `preventWebhook` | boolean | no | Whether to suppress LoginRadius webhook processing for the delete operation. Example: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `DELETE /identity/v2/auth/customobject/:objectrecordid` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-object-by-id.md) for the provider-specific parameters and requirements.

