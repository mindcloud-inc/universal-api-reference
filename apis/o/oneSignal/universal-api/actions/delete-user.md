# OneSignal: Delete User

Deletes a user from OneSignal.

```
DELETE https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/delete-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/delete-user?connectionId=$CONNECTION_ID&aliasId=string&aliasLabel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aliasId": "string",
  "aliasLabel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/delete-user?${params}`, {
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
| `aliasId` | string | yes | The alias value for the selected alias label. |
| `aliasLabel` | string | yes | The alias namespace to look up, such as external_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identity": {
        "onesignalId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identity.onesignalId` | string |  |

## Native endpoint

Through the native OneSignal API, this operation is `DELETE /apps/:app_id/users/by/:alias_label/:alias_id` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user.md) for the provider-specific parameters and requirements.

