# UseINBOX: Get All Custom Fields

Retrieves custom fields from UseINBOX.

```
GET https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-all-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-all-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-all-custom-fields?${params}`, {
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
      "createTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "Name": "Ava Chen",
      "Type": 1,
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date |  |
| `id` | string |  |
| `Name` | string |  |
| `Type` | number |  |
| `updateTime` | date |  |

## Native endpoint

Through the native UseINBOX API, this operation is `GET /inbox/v1/customfields` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-custom-fields.md) for the provider-specific parameters and requirements.

