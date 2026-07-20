# Sendbird: Delete Group Channel Custom Type



```
DELETE https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/delete-group-channel-custom-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/delete-group-channel-custom-type?connectionId=$CONNECTION_ID&customType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/delete-group-channel-custom-type?${params}`, {
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
| `customType` | string | yes | The group channel custom type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customType` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `DELETE /group_channels/custom_types/:customType` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group-channel-custom-type.md) for the provider-specific parameters and requirements.

