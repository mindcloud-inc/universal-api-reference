# INBOX: Get All Groups

Retrieves all group records from INBOX.

```
GET https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-all-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a INBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-all-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-all-groups?${params}`, {
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
      "resultCode": 1,
      "resultMessage": "string",
      "resultObject": {},
      "resultStatus": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultCode` | number |  |
| `resultMessage` | string |  |
| `resultObject` | object |  |
| `resultStatus` | boolean |  |
| `version` | string |  |

## Native endpoint

Through the native INBOX API, this operation is `GET /inbox/v1/groups` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-groups.md) for the provider-specific parameters and requirements.

