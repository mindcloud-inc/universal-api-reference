# Deputy: List States

Retrieves the state list from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-states?${params}`, {
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
      "_DPMetaData": {},
      "Active": true,
      "Code": "string",
      "Country": 1,
      "Created": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "Modified": "2026-05-07T12:00:00.000Z",
      "SortOrder": 1,
      "State": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_DPMetaData` | object |  |
| `Active` | boolean |  |
| `Code` | string |  |
| `Country` | number |  |
| `Created` | date |  |
| `Id` | number |  |
| `Modified` | date |  |
| `SortOrder` | number |  |
| `State` | string |  |

## Native endpoint

Through the native Deputy API, this operation is `POST /api/v1/resource/State/QUERY` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-states.md) for the provider-specific parameters and requirements.

