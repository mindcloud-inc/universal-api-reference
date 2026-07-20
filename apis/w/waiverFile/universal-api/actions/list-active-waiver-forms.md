# WaiverFile: List Active Waiver Forms

Retrieves active waiver forms from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-active-waiver-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-active-waiver-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-active-waiver-forms?${params}`, {
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
      "_currentInstance": {},
      "_WPObjectStatus": 1,
      "me": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_currentInstance` | object |  |
| `_WPObjectStatus` | number |  |
| `me` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetActiveWaiverForms` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-waiver-forms.md) for the provider-specific parameters and requirements.

